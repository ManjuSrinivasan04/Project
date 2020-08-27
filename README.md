IN – APP NOTIFICATION SYSTEM

OBJECTIVE  :
       To build a scalable in-app notification system for a sample classroom website. The users of this website will be students.This project mainly focus on students and instructors. This system allows instructor to share important data as well as notifications with students. It consists of a Instructor login along with student login. Instructor may upload course notifications through their provided login. The notifications are uploaded by faculty to different corresponding subset of students. We propose to build this system on an online server that allows instructor to upload data and students may view and search the notifications through their device. 

OVERALL DESCRIPTION:
Notifications are triggered when the following  happen :
                            1) A New course is available for a subset of students
                            2) A class wide notification is triggered by the staff
                            3) When a friend of a student completes a course
                            4) A remainder notification when one of enrolled courses is about to start
For the purpose of this project the website will contain a student login. After login it will contain a student profile page alone with his basic and academic detail. There will be an icon which when clicked will show a drop down list of unread notifications. This system able to maintain the entire history of notifications for a particular student.

SOFTWARE AND HARDWARE USED :

FRONTEND        :   Angular CLI: 10.0.2
                           Node: 12.18.2
                            OS: win32 x64
MIDDLEWARE  :   Java
DATABASE    :   MYSQL
TOOLS       :  Visual Studio Code and Eclipse


DATABASE TABLE STRUCTURE:

Course
Column	Type	Null	Default	Links to	Comments	MIME
ID (Primary)	int(11)	No				
name	varchar(20)	No				
couseID	varchar(20)	No				
StartDate	date	No				
EndDate	date	No				
Indexes
Keyname	Type	Unique	Packed	Column	Cardinality	Collation	Null	Comment
PRIMARY	BTREE	Yes	No	ID	0	A	No	

Friend
Column	Type	Null	Default	Links to	Comments	MIME
ID (Primary)	int(11)	No				
myID	int(11)	No				
friendID	int(11)	No				
Indexes
Keyname	Type	Unique	Packed	Column	Cardinality	Collation	Null	Comment
PRIMARY	BTREE	Yes	No	ID	0	A	No	

Groups
Column	Type	Null	Default	Links to	Comments	MIME
ID (Primary)	int(11)	No				
groupID	varchar(20)	No				
studentID	int(11)	No				
Indexes
Keyname	Type	Unique	Packed	Column	Cardinality	Collation	Null	Comment
PRIMARY	BTREE	Yes	No	ID	0	A	No	

Notification
Column	Type	Null	Default	Links to	Comments	MIME
ID (Primary)	int(11)	No				
message	varchar(20)	No				
courseID	varchar(20)	No				
StudentID	int(11)	No				
notificationID	int(11)	No				
Indexes
Keyname	Type	Unique	Packed	Column	Cardinality	Collation	Null	Comment
PRIMARY	BTREE	Yes	No	ID	0	A	No	

Staff
Column	Type	Null	Default	Links to	Comments	MIME
ID (Primary)	int(11)	No				
uname	varchar(20)	No				
pwd	varchar(20)	No				
Indexes
Keyname	Type	Unique	Packed	Column	Cardinality	Collation	Null	Comment
PRIMARY	BTREE	Yes	No	ID	0	A	No	

Students
Column	Type	Null	Default	Links to	Comments	MIME
ID (Primary)	int(11)	No				
username	varchar(20)	No				
password	varchar(20)	No				
studentID	varchar(20)	No				
department	varchar(20)	No				
Indexes
Keyname	Type	Unique	Packed	Column	Cardinality	Collation	Null	Comment
PRIMARY	BTREE	Yes	No	ID	0	A	No	

REASON TO CHOOSE MYSQL :
•	Speed - MySQL is fast. Its developers contend that MySQL is about the fastest database system you can get
•	Ease of use - MySQL is a high-performance but relatively simple database system and is much less complex to set up and administer than larger systems.
•	Query language support - MySQL understands SQL (Structured Query Language), the standard language of choice for all modern database systems.
•	Capability - The MySQL server is multi-threaded, so many clients can connect to it at the same time. Each client can use multiple databases simultaneously.
•	Connectivity and security - MySQL is fully networked, and databases can be accessed from anywhere on the Internet, so you can share your data with anyone, anywhere.
•	Portability - MySQL runs on many varieties of Unix, as well as on other non-Unix systems, such as Windows, NetWare, and OS/2.
•	Small size - MySQL has a modest distribution size, especially compared to the huge disk space footprint of certain commercial database systems.
•	Availability and cost - MySQL is an Open Source project with dual licensing.
•	Open distribution and source code - MySQL is easy to obtain; just use your Web browser. If you don't understand how something works, are curious about an algorithm, or want to perform a security audit, you can get the source code and examine it. If you think you've found a bug, report it; the developers want to know.

API AND FEATURES :

MAVEN : 

•	Maven is an automation and management tool.
•	It is written in Java Language and used to build and manage projects written in C#, Ruby, Scala, and other languages.
•	To configure the Maven, you need to use Project Object Model, which is stored in a pom.xml-file.
•	It is used for projects build, dependency and documentation. In short terms we can tell maven is a tool that can be used for building and managing any Java-based project.

REST API :
•	REST Client applications can use HTTP GET/POST methods to invoke Restful web services. REST doesn’t specify any specific protocol to use, but in almost all cases it’s used over HTTP/HTTPS. 
•	When compared to SOAP web services, these are lightweight and doesn’t follow any standard. We can use XML, JSON, text or any other type of data for request and response.

WEB SERVLET:
•	Servlets are Java classes which service HTTP requests and implement the javax.servlet.Servlet interface. 
•	A servlet is used to extend the capabilities of servers that host applications accessed by means of a request-response programming model.
•	 Although servlets can respond to any type of request, they are commonly used to extend the applications hosted by web servers.

MVC:
Model designs based on MVC architecture follow the MVC design pattern and they separate the application logic from the user interface when designing software. As the name implies MVC pattern has three layers, which are:
•	Model – Represents the business layer of the application
•	View – Defines the presentation of the application
•	Controller – Controller acts on both model and view. It controls the data flow into model object and updates the view whenever data changes. It keeps view and model separate.

JDBC:
•	JDBC stands for Java Database Connectivity. JDBC is a Java API to connect and execute the query with the database. 
•	It is a part of JavaSE (Java Standard Edition). JDBC API uses JDBC drivers to connect with the database.
STEPS : To connect Java application with the MySQL database, we need to follow  below steps.
•	Driver class: The driver class for the mysql database is com.mysql.jdbc.Driver.
•	Connection URL: The connection URL for the mysql database is jdbc:mysql://localhost:3360/cms where jdbc is the API, mysql is the database, localhost is the server name on which mysql is running, we may also use IP address, 3306 is the port number and cms is the database name. We may use any database, in such case, we need to replace the cms with our database name.
•	Username: The default username for the mysql database is root.
•	Password: It is the password given by the user at the time of installing the mysql database. 
ANGULAR MATERIAL :
•	Angular Material provides a set of reusable UI components based on the Material Design system. 
•	Angular Material is composed of several pieces. 
•	It has a CSS library for typography and other elements, it provides an interesting JavaScript approach for theming, and its responsive layout uses a flex grid.
ANGULAR :
•	Angular, supported by Google, is an open-source software engineering platform used for building user interfaces (front-end).
•	Angular 10 is a client-side TypeScript based framework which is used to create dynamic web applications.
•	Angular organizes code into buckets, whether it is components, directives, pipes, or services. Those who are familiar with Angular refer to these buckets as modules.

ANGULAR 10 FEATURES USED:
•	Modules
•	Routes
•	Services
•	Components
•	Directives
•	Material

TO INSTALL ANGULAR CLI:
 Run npm install @angular/cli  after the command finishes successfully, you should have Angular CLI installed.
DEVELOPMENT SERVER:
Run ng serve for a dev server. Navigate to  http://localhost:4200/. The app will automatically reload if you change any of the source files.
CODE SCAFFOLDING:
Run ng generate component component-name to generate a new component. You can also use ng generate directive|pipe|service|class|guard|interface|enum|module.
BUILD:
Run ng build to build the project. 





ADVANTAGES :
•	This project has a login page which allows only the registered Student to login and thereby preventing unauthorized access.
•	This system can be used to view all the notification details.
•	The Student will be able make quick view about their notifications anywhere using internet.
•	Usage of this application will be more helpful to the students to know about their courses.


GITHUB LINK:  https://github.com/Manju82/Project





