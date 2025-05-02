# E-commerce-project-springBoot
This project serves as an easy-to-understand setup for beginners , providing a base foundation in Spring Boot , MVC &amp; hibernate.


Old Version

issue: everytime connection open close for access database
https://github.com/Harshitaa109/E-commerce-project-springBoot/edit/main/README.md
New Version ( what's new)
Hibernate configuration added( database and tables automatically create when run the project)
Service classes provide reusable services throughout project
dao classes interact with database
bug fixed ( product image, security , etc..)
support in both eclipse & intellij ide
overall redesign entire code that help reusability.
disclaimer: currently working on this branch so there may be some bug related to endpoint, and working on cart logic.
Quickstart
Clone the repository
Open the project in your IDE: IntelliJ IDEA (recommended) or Eclipse
If you are using IntelliJ IDEA, make sure the IDE opens project as Maven and recognizes the project as a Spring Boot project. Also, you must change the working directory of the project so that the views (the actual web pages to be shown) are found by Spring Boot (check out Web Directories IntelliJ IDEA.
Make sure you are in the JtProject directory
Configure the database connection in application.properties file (check the Database section below for more info)
Run the project (by running the main method in JtSpringProjectApplication.java)
Open http://localhost:8080/ in your browser!
If you ran the basedata.sqlscript on the database, you can log in with the following credentials as admin; otherwise you'll have to manually create an admin user in the database:
Username: admin
Password: 123
Log in as a normal user:
Username: lisa
Password: 765
Database
MySQL or MariaDB can be used as the database for this project. The database connection can be configured in the src/main/resources/application.properties file, with the appropriate values for the following properties:

( You'd better use another username not root, and ensure that the user has the corresponding permissions for the database. )

    db.url=jdbc:mysql://[ip address of db]:[port of db]/ecommjava?createDatabaseIfNotExist=true
    db.username=[username]
    db.password=[password, if any]
if you met the error java.lang.IllegalArgumentException: Could not resolve placeholder 'db.driver' in value "${db.driver}", maybe you should change your mysql-connector-java version in pom.xml file according to your mysql version, don't forget to reload your Maven project.

Having done that, you must create some base data in the database. You can do that by running the basedata.sql script on the database. Check out Google for how to do that, because it depends on what tool you are using to access said database.

Web Directories
The views are located in src/main/webapp/views, but for some reason, Spring Boot doesn't recognize that directory. To remedy this, you must change the working directory of the project in your IDE. If you're using IntelliJ IDEA, follow these steps:

Click on the "Edit Configurations..." button in the top right corner of the IDE
Click on the JtSpringProjectApplication configuration
Change the "Working directory" option (if not present, click on "Modify Options" and select from the list) to the $MODULE_WORKING_DIR$ macro
Click "Apply" and "OK"
When you run the project, the views should be found by Spring Boot and you should see a login page in http://localhost:8080/ (if not logged in previously)! configurations

Workflow
image
Controller
control the endpoint and also send data to view( we use ModelAndView method)
  public String adminlogin() {
  	
  	return "adminlogin";
  }```
whenever /login url is hit , src->main->webapp-> adminlogin.jsp file execute
Models
represent data as entity and relationship among them.
View
receive data from controller and show with frontend.
Endpoints
http://localhost:8080/
http://localhost:8080/register
http://localhost:8080/admin/products
http://localhost:8080/admin/customers
http://localhost:8080/admin/categories
http://localhost:8080/admin/Dashboard
Spring Boot
For any information about Spring Boot, here are some useful links!

Reference Documentation
For further reference, please consider the following sections:

Official Apache Maven documentation
Spring Boot Maven Plugin Reference Guide
Create an OCI image
Spring Web
Guides
The following guides illustrate how to use some features concretely:

Building a RESTful Web Service
Serving Web Content with Spring MVC
Building REST services with Spring
Preview
![image](https://github.com/user-attachments/assets/1d49e15e-df93-48f3-ae06-fbb71a568dfc)

![image](https://github.com/user-attachments/assets/aeab64f0-bfea-4103-8e14-a1e173e68e45)

![image](https://github.com/user-attachments/assets/0cb0b965-fd87-40fc-92d1-020902e0b931)


Link
𝗬𝗼𝘂𝘁𝘂𝗯𝗲 𝗽𝗿𝗼𝗷𝗲𝗰𝘁 𝘃𝗶𝗱𝗲𝗼 𝗪𝗼𝗿𝗸𝗶𝗻𝗴 𝗗𝗲𝗺𝗼 + 𝘀𝘁𝗲𝗽 𝗯𝘆 𝘀𝘁𝗲𝗽 𝗲𝘅𝗲𝗰𝘂𝘁𝗶𝗼𝗻 𝗹𝗶𝗻𝗸 ( old version )::--- click here 
