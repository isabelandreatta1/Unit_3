# Database Unit3 Project 

**Table of Contents** 

1. Criteria A: [Planning]()
2. Criteria B: [Design]()
3. Criteria C: [Development]()
4. Criteria D: [Functionality]()
5. Criteria E: [Evaluation]()
6. [Appendix]()

## Criteria A: Planning 

### Identified Problem 
My client, Cathy, needs a new system for recording down her CAS activity for IB. She is currently using Managebac, however the features are very user unfriendly since it loads slowly, and the features needed are hard to find and difficult to navigate. The client, therefore, wants a system which is made specifically for recording CAS activity, which can also record the CAS activity in a calendar, . An additional issue my client has with Managebac is that it lacks a personalised interface, and so I will customise the new program to include a monkey theme because my client explicitly mentioned images of monkeys must be present to make it feel personal. 

### Proposed Solution 
My proposed solutions is to create a remote program using Python and the Kivy Library. The Kivy library provides a framework for both computer and phone applications, making it easy for the developer to implement a GUI (graphical user interface) in the application. This, in turn, makes the program much easier for the custotmer to use because they do not need to use the python console or terminal, but just the GUI screen provided. For the database itself, the data and tables will be stored and created using SQLAlchemy, and the relationships and queries will all be done using ORM (object-relational-mapping). Lastly, the program will include a log-in and registration feature, a page which the user can enter their CAS activities (date, activity name, activity type, and duration of activity all will be included), and 

**Designs** 

### Justification 

### Feasibility Report 

### Success Criteria 

## Criteria B: Design 

## Appendix 

Source Code: 

### Python File 
```py 
from sqlalchemy import Column, DateTime, String, Integer, ForeignKey
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import relationship
import sqlite3
from kivy.lang import Builder
from kivy.uix.behaviors import ButtonBehavior
from kivymd.app import MDApp
from kivy.uix.boxlayout import BoxLayout
from kivymd.uix.screen import MDScreen
from kivymd.uix.label import MDLabel
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker
from kivymd.uix.menu import MDDropdownMenu
from kivymd.uix.picker import MDDatePicker
from kivymd.uix.button import MDFillRoundFlatButton
from kivy.uix.relativelayout import RelativeLayout


Base = declarative_base()

class User(Base):
    __tablename__ = 'User'
    id= Column(Integer,primary_key=True,autoincrement=True)
    username= Column(String)
    password= Column(String)
    def __init__(self,username,password):
        self.username = username
        self.password = password

class CAS_Record(Base):
    __tablename__ = 'CAS'
    id = Column(Integer, primary_key = True, autoincrement = True)
    activity_name = Column(String)
    date = Column(DateTime)
    duration = Column(Integer)
    user_id = Column(Integer, ForeignKey('User.id'))

    def __init__(self, activity_name,date, duration):
        self.activity_name = activity_name
        self.date = date
        self.duration = duration

engine = create_engine('sqlite:///database.sqlite')
session = sessionmaker()
session.configure(bind=engine)
Base.metadata.create_all(engine)

class LoginScreen(MDScreen):

    def validate_user(self):
        self.ids.password_input.error = True
        self.ids.password_input.helper_text = "Incorrect username or password"
        print(self.ids.username_input.error)
        print(self.ids.username_input.helper_text)

    def try_login(self):
        username = self.ids.username_input.text
        password= self.ids.password_input.text
        Session = sessionmaker(bind = engine)
        session = Session()
        validate_user = session.query(User).filter_by(username = username, password = password).one_or_none()
        if validate_user:
            print("User exists")
            self.parent.current = "HomePage"

        else:
            print("User does not exist")
            self.validate_user()
        session.close()

class RegisterScreen(MDScreen):
    def try_register(self):
        username = self.ids.new_username_input.text
        password = self.ids.new_password_input.text
        password_confirm = self.ids.new_password_confirm.text
        if password == password_confirm:
            s = session()
            NewUser = User(username,password)
            s.add(NewUser)
            s.commit()
            s.close()
        else:
            print("Passwords don't match")

class HomePage(MDScreen):
    pass
    # create two buttons which will bring to either add entry page or calendar page

class ButtonLabel(ButtonBehavior, MDLabel):
    pass

class AddNewEntry(MDScreen):
    select_date = None

    def on_save(self, instance, value, date_range):
        '''
        Events called when the "OK" dialog box button is clicked.

        :type instance: <kivymd.uix.picker.MDDatePicker object>;

        :param value: selected date;
        :type value: <class 'datetime.date'>;

        :param date_range: list of 'datetime.date' objects in the selected range;
        :type date_range: <class 'list'>;
        '''

        print(value)
        AddNewEntry.select_date = value

    def on_cancel(self, instance, value):
        '''Events called when the "CANCEL" dialog box button is clicked.'''

    def show_date_picker(self):
        date_dialog = MDDatePicker()
        date_dialog.bind(on_save=self.on_save, on_cancel=self.on_cancel)
        date_dialog.open()

    def set_item(self, instance_menu, instance_menu_item):
        self.screen.ids.drop_down.set_item(instance_menu_item.text)
        instance_menu.dismiss()

    def drop_down_method(self):
        menu_items = ["10m","20m","30m","40m","50m","1h"]
        self.menu = MDDropdownMenu(
            caller = self.ids.drop_down,
            items = menu_items,
            position = "center",
            width_mult = 6,
        )
        self.menu.bind(on_release= self.set_item)

    def addEntry(self):
            activity_name = self.ids.activity_input.text
            duration = self.ids.duration_input.text
            activity = self.ids.activity_type
            creativity = self.ids.creativity_type
            add_date = AddNewEntry.select_date

            s = session()
            NewActivity = CAS_Record(activity_name, add_date, duration)
            s.add(NewActivity)
            s.commit()
            s.close()
            print("complete")
        #Add entry to the CAS activities
        #/2. Type of Activity (will change table), 3. time/duration 4. Date

class Calendar(MDScreen):
    def show_past_record(self):

        validate_user = session.query(User).filter_by().one_or_none()

class MainApp(MDApp):
    def build(self):
        self.theme_cls.primary_palette = "Amber"
        return

MainApp().run()



```

### Kivy File 
```
ScreenManager:
    id: scr_manager

    LoginScreen:
        name:"LoginScreen"

    RegisterScreen:
        name: "RegisterScreen"

    HomePage:
        name: "HomePage"

    AddNewEntry:
        name: "AddNewEntry"

    Calendar:
        name: "Calendar"

<LoginScreen>:
    BoxLayout:
        orientation: "vertical"
        size: root.height, root.width

        FitImage:
            source: "Background_DB.png"

    MDCard:
        size_hint: 0.6, 0.6 #relational to parent
        elevation: 10
        pos_hint: {"center_x": .5, "center_y": 0.5}
        orientation: "vertical"

        MDBoxLayout:
            id: content
            adaptive_height: True
            orientation: "vertical"
            padding: dp(10)
            spacing: dp(20)

            MDLabel:
                text: "Login"
                font_style: "H4"
                halign:"center"

            MDTextField:
                id: username_input
                hint_text: "Username"
                helper_text: "Invalid user"
                helper_text_mode: "on_error"
                required: True
                on_text_validate:
                    root.validate_user()

            MDTextField:
                id: password_input
                hint_text: "Password"
                icon_right: "eye-off"
                helper_text: "Invalid password"
                helper_text_mode:"on_error"
                required: True
                password: True

            MDRaisedButton:
                text: "Log in"
                on_release:
                    root.try_login()
                    print("button was pressed")

            MDRaisedButton:
                text: "Register"
                on_release:
                    root.parent.current = "RegisterScreen"

<RegisterScreen>:
    BoxLayout:
        orientation: "vertical"
        size: root.height, root.width
        FitImage:
            source: "Background_DB.png"

    MDCard:
        size_hint: 0.6, 0.6 #relational to parent
        elevation: 10
        pos_hint: {"center_x": .5, "center_y": 0.5}
        orientation: "vertical"

        MDBoxLayout:
            id: content
            adaptive_height: True
            orientation: "vertical"
            padding: dp(10)
            spacing: dp(20)

            MDLabel:
                text: "Register"
                font_style: "H4"
                halign:"center"

            MDTextField:
                id: new_username_input
                hint_text: "Username"
                helper_text: "Invalid user"
                helper_text_mode: "on_error"
                required: True

            MDTextField:
                id: new_password_input
                hint_text: "Password"
                icon_right: "eye-off"
                helper_text: "Invalid password"
                helper_text_mode:"on_error"
                required: True
                password: True

            MDTextField:
                id: new_password_confirm
                hint_text: "Confirm Password"
                icon_right: "eye-off"
                helper_text: "Invalid password"
                helper_text_mode:"on_error"
                required: True
                password: True

            MDFillRoundFlatButton:
                text: "Register"
                on_release:
                    root.try_register()

            MDFillRoundFlatButton:
                text: "Return"
                on_release:
                    root.parent.current = "LoginScreen"

<HomePage>:
    BoxLayout:
        orientation: "vertical"
        size: root.height, root.width
        FitImage:
            source: "Background_DB.png"

    MDCard:
        size_hint: 0.6, 0.6 #relational to parent
        elevation: 10
        pos_hint: {"center_x": .5, "center_y": 0.5}
        orientation: "vertical"

        MDBoxLayout:
            id: content
            adaptive_height: True
            orientation: "vertical"
            padding: dp(10)
            spacing: dp(20)

            MDLabel:
                text: "Welcome"
                font_style: "H4"
                halign:"center"

            MDRaisedButton:
                text: "Add entry"
                on_release:
                    root.parent.current = "AddNewEntry"

            MDRaisedButton:
                text: "Look at calendar"
                on_release:
                    root.parent.current = "Calendar"

<AddNewEntry>:
    BoxLayout:
        orientation: "vertical"
        size: root.height, root.width

    MDCard:
        size_hint: 0.6, 0.6 #relational to parent
        elevation: 10
        pos_hint: {"center_x": .5, "center_y": 0.5}
        orientation: "vertical"

        MDBoxLayout:
            id: content
            adaptive_height: True
            orientation: "vertical"
            padding: dp(10)
            spacing: dp(20)

            MDLabel:
                text: "Add Entry"
                font_style: "H4"
                halign:"center"

            MDTextField:
                id: activity_input
                hint_text: "Name of activity"
                helper_text: "Invalid activity"
                helper_text_mode:"on_error"
                required: True

            MDLabel:
                text:"Choose activity type"
                font_size: dp(15)

            MDRaisedButton:
                text:"Creativity"
                id: creativity_type
                group: "cas_type"
                pos_hint: {'center_x': 0.25, 'center_y': 0.5}
                on_release: self.background_color = (1, 0, 0, 1)

            MDRaisedButton:
                text:"Activity"
                id: activity_type
                group: "cas_type"
                pos_hint: {'center_x': 0.5, 'center_y': 0}
                on_release: self.background_color = (1, 0, 0, 1)

            MDRaisedButton:
                text:"Service"
                id: service_type
                group: "cas_type"
                pos_hint: {"center_x": 0.75, "center_y": 0}
                on_release: self.background_color = (1, 0, 0, 1)

            MDTextField:
                hint_text: "Duration of Activity in minutes"
                id: duration_input
                required: True

            MDRaisedButton:
                text: "Add Date"
                on_release: root.show_date_picker()

            MDFillRoundFlatButton:
                text: "Done"
                pos_hint: {'center_x': 0.8}
                on_release:
                    root.addEntry()

            MDRaisedButton:
                text: "Return"
                pos_hint: {'center_x': 0.2}
                on_release:
                    root.parent.current = "HomePage"

<Calendar>:
    BoxLayout:
        orientation: "vertical"
        size: root.height, root.width

        MDCard:
            size_hint: 0.6, 0.6 #relational to parent
            elevation: 10
            pos_hint: {"center_x": .5, "center_y": 0.5}
            orientation: "vertical"






```



