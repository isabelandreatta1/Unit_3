# Database Unit3 Project 

**Table of Contents** 

1. [Planning](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#criteria-a-planning)
2. [Design](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#criteria-b-design)
3. [Development]()
4. [Functionality]()
5. [Evaluation]()
7. [Appendix](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#appendix)
8. [Citation]()

## Criteria A: Planning 

### Identified Problem 

My client, Cathy, needs a new system for recording down her CAS activity for IB. She is currently using Managebac, however the features are very user unfriendly since it loads slowly, and the features needed are hard to find and difficult to navigate. The client, therefore, wants a system which is made specifically for recording CAS activity. An additional issue my client has with Managebac is that it lacks a personalised interface, and so I will customise the new program to include a monkey theme because my client explicitly mentioned images of monkeys must be present to make it feel personal. 

### Proposed Solution 

My proposed solutions is to create a remote program using Python and the Kivy Library. The Kivy library provides a framework for both computer and phone applications, making it easy for the developer to implement a GUI (graphical user interface) in the application. This, in turn, makes the program much easier for the custotmer to use because they do not need to use the python console or terminal, but just the GUI screen provided. For the database itself, the data and tables will be stored and created using SQLAlchemy, and the relationships and queries will all be done using ORM (object-relational-mapping). Lastly, the program will include a log-in and registration feature, a page which the user can enter their CAS activities (date, activity name, activity type, and duration of activity all will be included), and a page which the user can look at their previous records. After a consultation with the client, she approved. 
 
### Justification 

**Why Python and Kivy?**

Python is the most appropriate languaging to code in for this project. Other than the fact that, I, the developer, am most comfortable with it and thus will be able to create a more complex and elegant program, the language itself has several benefits. Firstly, it is currently the most popular programming language by a significant amount. According to PYPYL (Popularity of Programming Language), which measures each coding language's popularity by Google trends, concludes that python shares 30% of all computer language searches, while Java, the second most popular, shares only 18% [1]. Due to its popularity, this program can be easily understood by a larger number of developers and, furthermore, maintained. Python uses a simple syntax and offeres a wide variety of libraries -- add ons which can enhance your program with additional features [2]. The variety of libraries is very useful when needing to create a more complex program. However, there are a couple disadvantages to python. Pythonis a high-level language, meaning that it uses more abstraction and is less understandable to the computer as a trade off for having simple syntax . The consequences of this result in less control from the developer. Another disadvantage of python is that it does not run on a mobile application [2], but since the program will run on a computer, this does not interfere.


Kivy is a library created to work only for python. It is a framework which creates a GUI for the developer, which will mean the program will not run on the Python console or terminal, but via the GUI Screen. While Kivy uses its own language, it is simple, and will anyways need to run alongside with the python to write in the logic of the program. Kivy langauge organises its code with object-oriented-coding, which widgets and elements are classes [3]. The library is powerful because of the sheer number of features available, and is also supported for all devicess [4]. This allows my program to expand to multi-platforms if wanted. There are some significant set-backs with Kivy, such as major bugs with certain features, and little documentatioin available [4], but because my program will not recquire complex features, this will not have a significant impact. 

**Why SQLAlchemy and ORM?**

For the database, I will be using SQLAlchemy to create databases. SQLAlchemy is the python toolkit which works similarily like SQL but is in ORM. SQL is one of the most popular langue to interact with databases, with the ability of having almost all the functions related to data-table creating. SQLAlchemy is a more effiecient and simpler way of connecting to databases, with the advantage of obscuring or cutting down many of the tedious SQL tasks like connecting to servers and fetching data [5]. The reason why SQLAlchemy is so much more efficient is because it is an ORM (Object-relational-mapper), which make tasks (like querie) into objects. This result in a a high-level abstracted code. While in some cases it would be better to not obsscure some of the code with ORM, such as in a learning enviornment, for this project, it is preferred. 

### Feasibility Report 
**Technical Feasibility: Is there existing technology sufficient to implement the proposed solution?** 

The technical requirements for the proposed solutions are very low, as long as the client has a computer, she will not have an issue with accessing the program. Because Kivy is multi-platform, there are no specific needs for which type of computer. 

**Economical Feasibility: Is the proposed system cost-effective?** 

The program is extremely accessible and cost-effective. As mentioned previously, the only neccessary item is a computer (network not needed). 

**Legal Feasibility: Any conflicts between proposed system and regualtions/laws?** 

Kivy is free for both personal and commercial uses, so in that regard, there are no concerns about conflicts. Also, the project will remain small-scale and I have no intentions of getting the program copy-righted. 

**Operational Feasibility: Are there existing organisational practices and procedures sufficient to support the operation of the new proposed system?** 

While python is simple to understand and has many developers wellversed in it, the Kivy community remains small. This means that there are not many technicians which will be able to maintain it. But, Kivy is an easy language to understand if someone has knowledge of Python, and this project will be heavily documented on this Github repository. Also, the program is  simple so there will little need for maintanence.  

**Schedule Feasibility**: 

The project is due on April 1st, including development and documentatiton. This is feasible since we are provided approximately 3 weeks to work on it and the project has limited features. 

### Success Criteria 

1. Include the ability to input CAS activity
2.  Activity is categorised by Service, Activity and Creativity
3.  Record the time spent per activity
4.  Include 1 monkey in GUI and 2 personalised small icons 
5.  Include calender for choosing date 
6.  Record the accumulated time per category
7.  Include log-in with username and password

## Criteria B: Design 

###  Sketches 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/sketch_db.jpg" width=50% height=50%>

### System Flow Diagram 

### Flow Diagram 

### UML Diagram 
<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/UML.png" width=50% height=50%>

### ER Diagrams 
<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/ER_Diagram.png" width=50% height=50%>

### Normalised Tables 
<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/norm_table_1.png" width=50% height=50%>

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/norm_table_2.png" width=50% height=50%>

## Criteria C: Development 

- present the problem first
- write comments
- make sure variable names are meaningful 

### Login Screen 

***UI creation using Kivy*** 

The first part of creating the login screen is to design and code the UI (user interface). Without the actual UI,  the user will not be able to access the program. Since I am using Kivy, I have to use Kivy language. The way Kivy's UI works is that all the objects created are relative, and it's almost like layering paper on top of each other. The most fundamental and bottom "layer" is the screen. I want the screen to have a box layout and the size to be dynamic (meaning the user can change the screen size). Lastly, to create the bare sreen, I need to choose how objects will be placed in relation with each other; this is called orientation. I prefer to make it vertical so that every new element goes below the previous one. Once I created the basic screen, I wanted to add a pattern I drew for the background. After placing the png file in the project, I fit the image to the screen and refered the file name as the source of the background. 
```
ScreenManager:
    id: scr_manager

    LoginScreen:
        name:"LoginScreen"
        
<LoginScreen>:
    BoxLayout:
        orientation: "vertical"
        size: root.height, root.width
        FitImage:
            source: "Background_DB.png"
        
``` 

Size hint means the size as a relation to the parent, or the screen 
```
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
 ``` 
 
 Add label 
 ```
 MDLabel:
          text: "Login"
          font_style: "H4"
          halign:"center"MDLabel:
          text: "Login"
          font_style: "H4"
          halign:"center"

``` 

Text Field 

```

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
``` 
Buttons
```
            MDRaisedButton:
                text: "Log in"
                on_release:
                    root.try_login()
                    print("button was pressed")

            MDRaisedButton:
                text: "Register"
                on_release:
                    root.parent.current = "RegisterScreen"
                   
```


***Logic to create the screens*** 

```py

class LoginScreen(MDScreen):
    pass 
    
class MainApp(MDApp):
    def build(self):
        self.theme_cls.primary_palette = "Amber"
        return
        
        

```

***Creating tables with ORM*** 
```py
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
``` 

***Verifying user using database and logic behind Login*** 
```py
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
        session.close()class LoginScreen(MDScreen):

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
 ```

### Creating the Registration Screen 

UI creation is similar process of login screen 

***Adding user to database*** 
```py
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
```


### Creating the Home Page 

Just create a screen with two buttons. Most simplest aspect but very important 


### Creating the Add Entry Page 

Similar process of login screen but more complicated. 


### Creating the Past Entries Page 


## Criteria D: Functionality 


## Criteria E: Evaluation 



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

## Citations 

1. “PYPL PopularitY of Programming Language Index.” Github.io, 2019, pypl.github.io/PYPL.html.
2. Eastwood, Brian. “The 10 Most Popular Programming Languages to Learn in 2020.” Northeastern University Graduate Programs, 18 June 2020, www.northeastern.edu/graduate/blog/most-popular-programming-languages/.
3. “Kv Language — Kivy 2.0.0 Documentation.” Kivy.org, kivy.org/doc/stable/guide/lang.html. Accessed 21 Mar. 2021.
4. “What Is Kivy?” GeeksforGeeks, 28 Jan. 2020, www.geeksforgeeks.org/what-is-kivy/.



