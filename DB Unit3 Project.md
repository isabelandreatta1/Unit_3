# Database Unit3 Project 

**Table of Contents** 

1. [Planning](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#criteria-a-planning)
2. [Design](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#criteria-b-design)
3. [Development](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#criteria-c-development)
4. [Functionality](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#criteria-d-functionality)
5. [Evaluation](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#criteria-e-evaluation)
7. [Appendix](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#appendix)
8. [Citation](https://github.com/isabelandreatta1/Unit_3/blob/main/DB%20Unit3%20Project.md#citations)

## Criteria A: Planning 

### Identified Problem 

My client, Cathy, needs a new system for recording down her CAS activity for IB. She is currently using Managebac, however the features are very user unfriendly since it loads slowly, and the features needed are hard to find and difficult to navigate. The client, therefore, wants a system which is made specifically for recording CAS activity. An additional issue my client has with Managebac is that it lacks a personalised interface, and so I will customise the new program to include a monkey theme because my client explicitly mentioned images of monkeys must be present to make it feel personal. 

### Proposed Solution 

My proposed solutions is to create a remote program using Python and the Kivy Library. The Kivy library provides a framework for both computer and phone applications, making it easy for the developer to implement a GUI (graphical user interface) in the application. This, in turn, makes the program much easier for the custotmer to use because they do not need to use the python console or terminal, but just the GUI screen provided. For the database itself, the data and tables will be stored and created using SQLAlchemy, and the relationships and queries will all be done using ORM (object-relational-mapping). Lastly, the program will include a log-in and registration feature, a page which the user can enter their CAS activities (date, activity name, activity type, duration per activity). After a consultation with the client, she approved of this plan. 
 
### Justification 

**Why Python and Kivy?**

Python is the most appropriate languaging to code in for this project. Other than the fact that, I, the developer, am most comfortable with it and thus will be able to create a more complex and elegant program, the language itself has several benefits. Firstly, it is currently the most popular programming language by a significant amount. According to PYPYL (Popularity of Programming Language), which measures each coding language's popularity by Google trends, concludes that python shares 30% of all computer language searches, while Java, the second most popular, shares only 18% [1]. Due to its popularity, this program can be easily understood by a larger number of developers and, furthermore, maintained. Python uses a simple syntax and offeres a wide variety of libraries -- add ons which can enhance your program with additional features [2]. The variety of libraries is very useful when needing to create a more complex program. However, there are a couple disadvantages to python. Pythonis a high-level language, meaning that it uses more abstraction and is less understandable to the computer as a trade off for having simple syntax . The consequences of this result in less control from the developer. Another disadvantage of python is that it does not run on a mobile application [2], but since the program will run on a computer, this does not interfere.


Kivy is a library created to work only for python. It is a framework which creates a GUI for the developer, which will mean the program will not run on the Python console or terminal, but via the GUI Screen. While Kivy uses its own language, it is simple, and will anyways need to run alongside with the python to write in the logic of the program. Kivy langauge organises its code with object-oriented-coding, which widgets and elements are classes [3]. The library is powerful because of the sheer number of features available, and is also supported for all devicess [4]. This allows my program to expand to multi-platforms if wanted. There are some significant set-backs with Kivy, such as major bugs with certain features, and little documentatioin available [4], but because my program will not recquire complex features, this will not have a significant impact. 

**Why SQLAlchemy and ORM?**

For the database, I will be using SQLAlchemy to create databases. SQLAlchemy is the python toolkit which works similarily like SQL but is in ORM. SQL is one of the most popular langue to interact with databases, with the ability of having almost all the functions related to data-table creating. SQLAlchemy is a more effiecient and simpler way of connecting to databases, with the advantage of obscuring or cutting down many of the tedious SQL tasks like connecting to servers and fetching data [5]. The reason why SQLAlchemy is so much more efficient is because it is an ORM (Object-relational-mapper), which make tasks (like queries) into objects. This results in a a high-level abstracted code. While in some cases it would be better to not obsscure some of the code with ORM, such as in a learning enviornment, for this project, it is preferred. 

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
4.  Include 1 monkey in UI 
5.  Include calender for choosing date 
6.  Include log-in with username and password

## Criteria B: Design 

###  Sketches 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/sketch_db.jpg" width=50% height=50%>

*Figure 1: A draft sketch of the UI screen and screen flow chart*

### Code Flow Diagrams: 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/RegisterScreen_Flow.png" width=50% height=50%>

*Figure 2: Flow diagram of the registration screen* 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/LoginScreen_Flow.png" width=50% height=50%>

*Figure 3: Flow diagram of the login screen* 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Register_Screen_Flow.png" width=75% height=75%>

*Figure 4: Flow diagram of the add entry screen* 

### System Flow Diagram 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/system_diagram.png" width=50% height=50%>

*Figure 5: System flow diagram with the inputs, outputs and flow of information* 

### UML Diagram 
<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/UML.png" width=50% height=50%>

*Figure 6: Above is a UML Diagram of the program database. It shows each classes' attributes and their relationship. For each User, they can have n number of CAS activities* 

### ER Diagrams 
<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/ER_Diagram.png" width=50% height=50%>

*Figure 7: Above is an ER Diagraam*

### Normalised Tables 
<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/norm_table_1.png" width=50% height=50%>

*Figure 8: Normalised tables for User Information and CAS Record Information. They have beeen normalised until the third form, which means that each record is unique, each cell contains a value, includes a single column primary key, and each column is independent *

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/norm_table_2.png" width=50% height=50%>

*Figure 9: Normalised table for the relationship between User Information and CAS Record Information.*

## Criteria C: Development 

### Login Screen 

***UI creation using Kivy*** 

The first part of creating the login screen is to design and code the UI (user interface). Without the actual UI,  the user will not be able to access the program. Since I am using Kivy, I have to use Kivy language. The way Kivy's UI works is that all the objects created are relative, and it's almost like layering paper on top of each other. The bottom "layer" is the screen. I want the screen to have a box layout and the size to be dynamic (meaning the user can change the screen size). Lastly, to create the bare sreen, I need to choose how objects will be placed in relation with each other; this is called orientation. I prefer to make it vertical so that every new element goes below the previous one. Once I created the basic screen, I wanted to add a pattern I drew for the background. After placing the png file in the project, I fit the image to the screen and refered the file name as the source of the background. 
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
I then to have a place to put all my elements inside, I do this by creating an MDCard and an MDBox. 
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
 Now that I have the basic screen created, I need to write in all the text. I first do this by adding a Login Label. 
 ```
 MDLabel:
          text: "Login"
          font_style: "H4"
          halign:"center"MDLabel:
          text: "Login"
          font_style: "H4"
          halign:"center"
``` 

Next, I need a place for the user to input their username and password. This is called a textfield. There are certain properties of textfield which are quite useful, such as making the input "required" or having a message pop-up if there is an error (this is called helper text). Once the user inputs their username and password, I ned to validate that the user account exists. I do this by creating a method in python and calling it once validating the text. 

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
Lastly, I need to create the buttons. There are two buttons needed: the login buton and the register button. The login button will validate the user while register button will change to the registration screen. The way I create the login button is by creating a method in python and calling it once the button is pressed, while I can just changeto the Register Screen once the register button is pressed. 

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

I've created the Kivy file to creat a UI but there is no logic which will make any of the functions work. To fix this, I need a complimentary Python file which will make my program work. The most fundamental and basic python code you need is a class to create all the screens and thee app itself. I addede the Amber theme to my app, which is part of the Kivy library. This will result in many of my widgets using an amber colour palette. 
```py
class LoginScreen(MDScreen):
    pass 
    
class MainApp(MDApp):
    def build(self):
        self.theme_cls.primary_palette = "Amber"
        return  
```

I've created the program but I now need a database which collect user information, such as user accounts, and CAS activity. I will use ORM in order to expedite and abstract much of the query process. 

Based on my diagrams and plan, I know I need to tables:  a user table and a CAS activity table. I simply create two classes for each table, and write down their attributes. Each one will have their own primary key, which autoincrements, while the other values are input by the user. The benefit of using SQLAlchemy is that it makes relationships much easier: instead of creating a third table to establish their relationship (as shown in my normalisation tables), I can simply use a foreign key by referencing the user IDs and connecting them as such. 

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
After creating the data tables, I need a way to be able to input values in it and also to create the logic behind the login process. Within the LoginScreen, I create all the methods which will used when logging in. 

The first thing I need to do is connect the database to the input, and query to see if the username and password exists in the database. If the password and username correspond to values in the User table, then the screen will change to the Homepage. However, if the user does not exist, then a message will tell the user that the username or password is incorrect. To show this message, I will create a method which will assert an error, and then the text "incorrect username or password" will show on the screen.

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
        session.close()
 ```

### Creating the Registration Screen 

Next, I need to create a registration screen since a user can not login without registering an account. For the UI (or Kivy file) and the start-up Python file (i.e creating class for screen) is very similar as the process of coding the login screen; the new step is to add the user input to the database. To ensure that the user does not make any mistakes while making their account, I added a second password input text field so that they can confirm they put the same password. If both passwords are equal to each other, then the code creates a new session in the database, and inputs the username and password values in the User table. If they do not match, then I need some type of indicator so the user is aware of the error. I did so by adding a message in the python console. 

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
### Hashing Passwords 

Hash functions are functions that convert any length input into fixed-length encrypted string. This is very valuable to secure a database because vulnerable information, because usually hash values are always unique and hard to interpret (no matter if a novel or word, they will always result in the same length value so hackers will not know the actual length of the original input), the brute force method of "decyphering" a hash value makes it almost impossible because of the high computational power and time needed.

To hash the passwords, I need to have two functions. The first function needs to hash the password during the register screen, and the second function checks if the password input during the login processs is the same as the hash in the data base. 

The first function, which is caalled ```hash_password``` focuses on doing two things: hashing the password and hashing/adding a salt. A salt is a random value which is added to the password, which then further encrypts the password and makes it difficult for external parties to crack the password. 

The second function, ```verify_password``` instead works on comparing the hash with the 

```py
def verify_password(stored_password, password):
        """Verify a stored password against one provided by user"""
        salt = stored_password[:64]
        stored_password = stored_password[64:]
        #here it encodees the password
        pwdhash = hashlib.pbkdf2_hmac('sha256',password.encode('utf-8'),salt.encode('ascii'),100000)
        pwdhash = binascii.hexlify(pwdhash).decode('ascii')
        #check  if password is the  same as stored password
        return pwdhash == stored_password

    #login method
    def try_login(self):
        #ids from Kivy file and rename them as simple variables
        username = self.ids.username_input.text
        password = self.ids.password_input.text
        Session = sessionmaker(bind=engine)
        session = Session()
        #query to see if the user input and password input exists in the tbale
        validate_user = session.query(User).filter_by(username=username).one_or_none()

        #if the query result exists then...
        if validate_user:
            print("User exists")
            #variabale for user_id which can be called from outside of this class
            LoginScreen.user_id = validate_user.id
            #query to check if password is  correct
            stored_password = session.query(User).get(validate_user.id).password
            print(stored_password)
            print(password)
            print(LoginScreen.verify_password(stored_password,password))
            if LoginScreen.verify_password(stored_password, password) == True:
                #screen changes to home Page
                self.parent.current = "HomePage"
                
                
class RegisterScreen(MDScreen):

    def hash_password(self):
        password = self.ids.new_password_input.text
        """Hash a password for storing."""
        salt = hashlib.sha256(os.urandom(60)).hexdigest().encode('ascii') #hashing a ramdom sequence with 60 bits: produces 256 bits or 64 hex chars
        pwdhash = hashlib.pbkdf2_hmac('sha256',password.encode('utf-8'),salt, 100000)
        pwdhash = binascii.hexlify(pwdhash) #hashing the password with the salt producing 256 bits or 64 hex chars
        return (salt + pwdhash).decode('ascii') #total lenght is 128 chars or 512 bits

    def try_register(self):
        username = self.ids.new_username_input.text
        input_password = self.ids.new_password_input.text
        #have a confirm password to make sure the user input password correctly
        password_confirm = self.ids.new_password_confirm.text
        #if both password input are equal
        hashed_password = RegisterScreen.hash_password(self)
        if input_password == password_confirm:
            s = session()
            #add the username and password to the User table
            NewUser = User(username, hashed_password)
            s.add(NewUser)
            s.commit()
            s.close()

```
### Creating the Home Page 

For the home page, I just need to create a screen with one button. The button will bring the user to the add CAS activity screen. The home page is just a matter of repeating the same elements as my previous ones. 


### Creating the Add Entry Page 

The add entry page is the most important aspect of my program since it is the purpose of this project. The user must be able to input a variety of items, including: 1. CAS activity name 2. Type of activity (choose from Creativity, Activity, Service), 3. Duration of activity 4. Date. For the activity name and the duration of activity, I will make both values into text fields (or user inputs) because each activity has a unique value. However, for the date and type of activity, I want the user to press a button instead of inputting a value so, not only is the process easier, but it reduces chances of the user writing the information incorrectly. If the user uses a button, the program has a standard format for type of activity and date. 

Firstly, I create a method which will add the entry. The acitivty name and duration are user inputs. For the date, I will use a date picker widget. It looks like the figure below. 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/DatePickerWidget.png" width=50% height=50%>

*Figure 10: Date picker widget sample* 

This makes the date format standard, and is much more user friendly than having to type the input. To use this widget, I need to create two additional methods: on_save and on_cancel. These methods must be included when using the datePicker widget because the on_save method will save the date value selected, while the on cancel method will delete all new changes. 

```py
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
``` 

While for the cas type, I will have each CAS category as a button. One of Kivy button behaviours is that, when a button is pressed, the button state is down, and when the button is not pressed, then the button state is normal. On the release of the button press, a method will check which button's state is down (which was pressed), and then assign the cas activity variable.

```py
    def check_cas_type(self):
        if self.ids.creativity_type.state == "down":
            self.cas_type = "Creativity"
            print(self.cas_type)
        elif self.ids.activity_type.state == "down":
            self.cas_type = "Activity"
            print(self.cas_type)
        elif self.ids.service_type.state == "down":
            self.cas_type = "Service"
            print(self.cas_type)
 ```
 
 The very last step of my program is to add all the cas information to the database. In addition to the user inputs, the user_id also needs to be included. For the user_id, I call the user_id variable I created in the login screen. This makes sure that the user_id is the same as the logged in user. Then, I put the information in the CAS record database. With that, my program's basic functionality is complete. 
 
```py

    def addEntry(self):
        activity_name = self.ids.activity_input.text
        duration = self.ids.duration_input.text
        add_date = AddNewEntry.select_date
        cas_type = self.cas_type
        user_id = LoginScreen.user_id
        print(user_id)
        print(cas_type)
        s = session()
        NewActivity = CAS_Record(activity_name, add_date, duration, cas_type, user_id)
        s.add(NewActivity)
        s.commit()
        s.close()
        print("complete")
``` 
### UI Screenshots 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Saved.png" width=50% height=50%>
*Figure 11: Above is a screenshot of the saved button. This page appears once a new entry has been saved to the data base*

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Login.png" width=50% height=50%>

*Figure 12: Above is a screenshot of the login page*

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/HomePAge.png " width=50% height=50%>

*Figure 13: Above is a screenshot of the home page*


## Criteria D: Functionality 

https://drive.google.com/file/d/1uiGoPknZZWblvtDjy1pMCVxiAxIvHRAg/view?usp=sharing 

Above is my functionality video. 

## Criteria E: Evaluation 

### Alpha Testing 

| Step                   | Input                                                                                                                                                     | Output                                                                          | Success Criteria                                                                                                    | Success |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------|
| 1. Register User Error | Username, non-matching confirm password and password                                                                                                      | Text stating "Passwords don't match"                                            | Include log-in with username and password                                                                           | Yes     |
| 2. Register User       | Username, confirm password and password                                                                                                                   | Text input in box and  user information stored in  User database                | Include log-in with username and password                                                                           | Yes     |
| 3. Login User Error    | Incorrect username and password                                                                                                                           | Text stating "Incorrect username or password" when pressing password text field | Include log-in with username and password                                                                           | Yes     |
| 4. Login User          | Registered username and password                                                                                                                          | Home Page appears                                                               | Include log-in with username and password                                                                           | Yes     |
| 5. Add Entry           | Input text in activity, duration, press the desired button for CAS activity, click the date of event. Repeat three times to check if all sections works.  | Text inputed in boxes                                                           | Include the ability to input CAS activity,  Record the time spent per activity,  Include calender for choosing date | Yes     |
| 6. Save Entry          | Press "Done" Button                                                                                                                                       | Entry and information saved in CAS Records database with the correct  user ID   | Activity is categorized by Service, Activity and Creativity                                                         | Yes     |
| 7. Cancel Entry        | Repeat Add entry process but instead of pressing done,  press return                                                                                      | None of the inputs from the entry are saved in the database                     | Include the ability to input CAS activity                                                                           | Yes     |
| 8. Save Entry          | Press "Done" Button                                                                                                                                       | Screen with a picture of a monkey  should appear                                | Include 1 monkey in GUI                                                                                             | Yes     |
|                        |                                                                                                                                                           |                                                                                 |                                                                                                                     |         |

###  Unit Testing 

**Unit Testing for the Hash Passwords Register Screen** 

In order to test if the hash password is working for the register screen, I created a table just for the register screen hashed passwords. The new data table will have two columns: input passwords and hashed password. This way I can make sure that the input password is correct, that it is hashing the password, and that it is successfully saving in the data base. I put 5 different inputs and then checked what saved on the database. I also disabled the login function just to ensure I was only checking the hash password for register screen. Below is the results of the table: 

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/UnitTesting_Hash.png" width=50% height=50%>

*Figure 13: Data Table Hashed Password* 

| Test Number | Input  | Is the input saved correctly? | Is the length of the hashed password 128 characters? |
|-------------|--------|-------------------------------|------------------------------------------------------|
| 1           | test   | Yes                           | Yes                                                  |
| 2           | 123    | Yes                           | Yes                                                  |
| 3           | !!!    | Yes                           | Yes                                                  |
| 4           | a      | Yes                           | Yes                                                  |
| 5           | monkey | Yes                           | Yes                                                  |

Because it is too complicated to check if the password was hashed correctly, a way to circumvent this is to check if the length of the stored password is 128 characters. This is because any text that is hashed turns to 64 Hex character length. Because the stored password is addded with the salt, this means the length of the storede password must be 128 characters (or 64 + 64 characters). 

As seen from the test above, it can be concludued that the register screen hashing is successful. 

```py
 def try_login(self):
        #ids from Kivy file and rename them as simple variables
        username = self.ids.username_input.text
        password = self.ids.password_input.text
        Session = sessionmaker(bind=engine)
        session = Session()
        #query to see if the user input and password input exists in the tbale
        validate_user = session.query(User).filter_by(username=username).one_or_none()

        #if the query result exists then...
        if validate_user:
            print("User exists")
            #variabale for user_id which can be called from outside of this class
            LoginScreen.user_id = validate_user.id
            #query to check if password is  correct
            stored_password = session.query(User).get(validate_user.id).password
            if LoginScreen.verify_password(stored_password, password) == True:
                #screen changes to home Page
                self.parent.current = "HomePage"  
```

### Beta Testing 

I had a person who was not involved with the development of this program to do the beta testing. They simply followed the input instructions and wrote an "X" in the success section if the correct output occured. 

| Step                   | Input                                                                                                                            | Output                                                                          | Success Criteria                                                                                                      | Success |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|---------|
| 1. Register User Error | Input "test" for username, "test" for password and "badtest" for confirm password                                                | Text stating "Passwords don't match"                                            | Include log-in with username and password                                                                             | X       |
| 2. Register User       | Input "test" for username, password and confirm password                                                                         | "test" stored in  User database                                                 | Include log-in with username and password                                                                             | X       |
| 3. Login User Error    | Input "test" for username and "badtest" for password                                                                             | Text stating "Incorrect username or password" when pressing password text field | Include log-in with username and password                                                                             | X       |
| 4. Login User          | Input "test" for both username and password                                                                                      | Home Page appears                                                               | Include log-in with username and password                                                                             | X       |
| 5. Add Entry           | Input "Football activity" for cas name, "March 15 2018" for date, "20 minutes"  for duration, and click "Activity" for cas type  | Text inputed in boxes                                                           | Include the ability to input CAS activity,   Record the time spent per activity,   Include calender for choosing date | X       |
| 6. Save Entry          | Press "Done" Button                                                                                                              | Entry and information saved in CAS Records database with the correct  user ID   | Activity is categorized by Service, Activity and Creativity                                                           | X       |
| 7. Cancel Entry        | Repeat Add entry process but instead of pressing done,  press return                                                             | None of the inputs from the entry are saved in the database                     | Include the ability to input CAS activity                                                                             | X       |
| 8. Save Entry          | Press "Done" Button                                                                                                              | Screen with a picture of a monkey  should appear                                | Include 1 monkey in GUI                                                                                               | X       |

### Extent and Limitations of Program 
- 

## Appendix 

### Conversations with client  

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Client_Talk_1.png" width=50% height=50%>

Figure : Above is one of the recorded conversations with my client to understand the purpose of the program

<img src="https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Client_Talk_2.png" width=50% height=50%>

Figure: This imaage shows that my client approves of the success criteria we created together 

### Source Code 

***Python File*** 
```py
from sqlalchemy import Column, DateTime, String, Integer, ForeignKey, desc
from sqlalchemy.ext.declarative import declarative_base
from kivy.uix.behaviors import ButtonBehavior
from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen
from kivymd.uix.label import MDLabel
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker
from kivymd.uix.picker import MDDatePicker
import hashlib, binascii, os
from sqlalchemy import and_
Base = declarative_base()

# create User table

class User(Base):
    __tablename__ = 'User'
    id = Column(Integer, primary_key=True, autoincrement=True)
    username = Column(String)
    password = Column(String)

    #initaliser will need username and password when adding values to table
    def __init__(self, username, password):
        self.username = username
        self.password = password

# create CAS record table
class CAS_Record(Base):
    __tablename__ = 'CAS'
    id = Column(Integer, primary_key=True, autoincrement=True)
    activity_name = Column(String)
    date = Column(DateTime)
    duration = Column(Integer)
    cas_type = Column(String)
    # need foreign key to create relationship between user and CAS activity
    user_id = Column(Integer, ForeignKey('User.id'))

    def __init__(self, activity_name, date, duration, cas_type, user_id):
        self.activity_name = activity_name
        self.date = date
        self.duration = duration
        self.cas_type = cas_type
        self.user_id = user_id


#this creates the tables
engine = create_engine('sqlite:///database.sqlite')
session = sessionmaker()
session.configure(bind=engine)
Base.metadata.create_all(engine)

#create class for Login screen
class LoginScreen(MDScreen):
    user_id = None
    stored_password = None
    #asssert error method
    def validate_user(self):
        self.ids.password_input.error = True
        #will show helper text if there is an error
        self.ids.password_input.helper_text = "Incorrect username or password"

    def verify_password(stored_password, password):
        """Verify a stored password against one provided by user"""
        salt = stored_password[:64]
        stored_password = stored_password[64:]
        #here it encodees the password
        pwdhash = hashlib.pbkdf2_hmac('sha256',password.encode('utf-8'),salt.encode('ascii'),100000)
        pwdhash = binascii.hexlify(pwdhash).decode('ascii')
        #check  if password is the  same as stored password
        return pwdhash == stored_password

    #login method
    def try_login(self):
        #ids from Kivy file and rename them as simple variables
        username = self.ids.username_input.text
        password = self.ids.password_input.text
        Session = sessionmaker(bind=engine)
        session = Session()
        #query to see if the user input and password input exists in the tbale
        validate_user = session.query(User).filter_by(username=username).one_or_none()

        #if the query result exists then...
        if validate_user:
            print("User exists")
            #variabale for user_id which can be called from outside of this class
            LoginScreen.user_id = validate_user.id
            #query to check if password is  correct
            stored_password = session.query(User).get(validate_user.id).password
            print(stored_password)
            print(password)
            print(LoginScreen.verify_password(stored_password,password))
            if LoginScreen.verify_password(stored_password, password) == True:
                #screen changes to home Page
                self.parent.current = "HomePage"

        else:
            #print message on python console
            print("User does not exist")
            self.validate_user()
            #error occurs
        session.close()

#creaate class fo Registration Screen
class RegisterScreen(MDScreen):

    def hash_password(self):
        password = self.ids.new_password_input.text
        """Hash a password for storing."""
        salt = hashlib.sha256(os.urandom(60)).hexdigest().encode('ascii') #hashing a ramdom sequence with 60 bits: produces 256 bits or 64 hex chars
        pwdhash = hashlib.pbkdf2_hmac('sha256',password.encode('utf-8'),salt, 100000)
        pwdhash = binascii.hexlify(pwdhash) #hashing the password with the salt producing 256 bits or 64 hex chars
        return (salt + pwdhash).decode('ascii') #total lenght is 128 chars or 512 bits

    def try_register(self):
        username = self.ids.new_username_input.text
        input_password = self.ids.new_password_input.text
        #have a confirm password to make sure the user input password correctly
        password_confirm = self.ids.new_password_confirm.text
        #if both password input are equal
        hashed_password = RegisterScreen.hash_password(self)
        if input_password == password_confirm:
            s = session()
            #add the username and password to the User table
            NewUser = User(username, hashed_password)
            s.add(NewUser)
            s.commit()
            s.close()
        else:
            #if the passwords don't match, then messsage will print on console
            print("Passwords don't match")

class HomePage(MDScreen):
    #nothing needed for the Home page
    pass

class SavedBackground(MDScreen):
    #nothing needed for the home page
    pass

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
        #create value so I can recall in another method

    def on_cancel(self, instance, value):
        '''Events called when the "CANCEL" dialog box button is clicked.'''
        print("cancel")

    def show_date_picker(self):
        date_dialog = MDDatePicker()
        date_dialog.bind(on_save=self.on_save, on_cancel=self.on_cancel)
        date_dialog.open()
        #method to create datePicker widget

    def check_cas_type(self):
        #if condition to see which buttonns are pressed
        if self.ids.creativity_type.state == "down":
            #down state means button pressed
            self.cas_type = "Creativity"
            print(self.cas_type)
        elif self.ids.activity_type.state == "down":
            self.cas_type = "Activity"
            print(self.cas_type)
        elif self.ids.service_type.state == "down":
            self.cas_type = "Service"
            print(self.cas_type)

    def addEntry(self):
        activity_name = self.ids.activity_input.text
        duration = self.ids.duration_input.text
        add_date = AddNewEntry.select_date
        cas_type = self.cas_type
        user_id = LoginScreen.user_id
        print(user_id)
        print(cas_type)
        s = session()
        #add activity to records
        NewActivity = CAS_Record(activity_name, add_date, duration, cas_type, user_id)
        s.add(NewActivity)
        s.commit()
        s.close()
        print("complete")

class MainApp(MDApp):
    def build(self):
        self.theme_cls.primary_palette = "Amber"
        return

MainApp().run()

``` 

***Kivy File*** 
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

    SavedBackground:
        name: "SavedBackground"

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
        size_hint: 0.75, 0.75 #relational to parent
        elevation: 10
        pos_hint: {"center_x": .5, "center_y": 0.5}
        orientation: "vertical"
        FitImage:
            source: "homepage.jpg"

        MDBoxLayout:
            id: content
            adaptive_height: True
            orientation: "vertical"

            MDLabel:
                text: "Welcome"
                font_style: "H4"
                halign:"center"

            MDFillRoundFlatButton:
                text: "Add entry"
                pos_hint: {'center_x': 0.2}
                on_release:
                    root.parent.current = "AddNewEntry"

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
            spacing: dp(10)

            MDLabel:
                text: "Add Entry"
                font_style: "H4"
                halign:"center"

            MDBoxLayout:
                id: content
                adaptive_height: True
                orientation: "horizontal"
                spacing: dp(50)
                padding: dp(20)

                MDTextField:
                    id: activity_input
                    hint_text: "Name of activity"
                    helper_text: "Invalid activity"
                    helper_text_mode:"on_error"
                    required: True

                MDFillRoundFlatButton:
                    text: "Add Date"
                    on_release: root.show_date_picker()

                MDTextField:
                    hint_text: "Duration of Activity"
                    id: duration_input
                    required: True

            MDBoxLayout:
                id: content
                adaptive_height: True
                orientation: "horizontal"
                padding: dp(20)
                spacing: dp(100)

                MDFillRoundFlatButton:
                    text:"Creativity"
                    id: creativity_type
                    on_press:
                        root.check_cas_type()

                MDFillRoundFlatButton:
                    text:"Activity"
                    id: activity_type
                    on_press:
                        root.check_cas_type()

                MDFillRoundFlatButton:
                    text:"Service"
                    id: service_type
                    on_press:
                        root.check_cas_type()

            MDBoxLayout:
                id: content
                adaptive_height: True
                orientation: "horizontal"
                spacing: dp(330)

                MDRoundFlatButton:
                    text: "Done"
                    on_release:
                        root.addEntry()
                        root.parent.current = "SavedBackground"

                MDRoundFlatButton:
                    text: "Return"
                    on_release:
                        root.parent.current = "HomePage"

<SavedBackground>:
    BoxLayout:
        orientation: "vertical"
        size: root.height, root.width
        FitImage:
            source: "save_background.png"

        MDFillRoundFlatButton:
            text: "Return"
            pos_hint: {'center_x': 0.8}
            on_release:
                root.parent.current = "HomePage"
```

## Citations 

1. “PYPL PopularitY of Programming Language Index.” Github.io, 2019, pypl.github.io/PYPL.html.
2. Eastwood, Brian. “The 10 Most Popular Programming Languages to Learn in 2020.” Northeastern University Graduate Programs, 18 June 2020, www.northeastern.edu/graduate/blog/most-popular-programming-languages/.
3. “Kv Language — Kivy 2.0.0 Documentation.” Kivy.org, kivy.org/doc/stable/guide/lang.html. Accessed 21 Mar. 2021.
4. “What Is Kivy?” GeeksforGeeks, 28 Jan. 2020, www.geeksforgeeks.org/what-is-kivy/.



