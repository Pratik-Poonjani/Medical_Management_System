# Medical_Management_System

##   Overview
The Medical Management System is a Java-based desktop application designed to manage medical records and appointments in a healthcare facility. It provides functionalities to store patient information, schedule appointments, manage medical staff, and generate reports.


## Features
#### 1. Patient Management
 - __Add, View, Update, Delete:__ Users can seamlessly manage patient records, including personal information, medical history, and contact details.
 - __Search Functionality:__ Allows users to search for specific patients based on various criteria such as name, age, gender, or medical condition.

#### 2. Appointment Scheduling
 - __Appointment Booking:__ Enables users to schedule appointments for patients with doctors or other medical staff members.
 - __Calendar View:__ Provides a visual representation of appointment schedules, making it easy for users to manage and track appointments.
 - __Reminder Notifications:__ Sends automated reminders to patients and staff members about upcoming appointments to reduce no-show rates.

#### 3. Medical Staff Management
 - __Add, View, Update, Delete:__ Facilitates the management of medical staff members, including doctors, nurses, technicians, and administrative personnel.
 - __Role Assignment:__ Allows administrators to assign roles and responsibilities to staff members based on their expertise and specialization.
 - __Departmental Organization:__ Supports the categorization of staff members into different departments or units for efficient management.

#### 4. Billing and Invoicing
 - __Generate Bills:__ Automatically calculates the cost of medical services provided to patients and generates itemized bills/invoices.
 - __Billing History:__ Maintains a comprehensive history of billing transactions for each patient, facilitating easy tracking and reconciliation.
 - __Payment Processing:__ Supports various payment methods and integrates with payment gateways for seamless payment processing.

#### 5. Reporting
 - __Customizable Reports:__ Provides predefined templates for generating reports on patient demographics, appointment schedules, billing summaries, and inventory status.
 - __Export Options:__ Allows users to export reports in multiple formats such as PDF, Excel, or CSV for further analysis and sharing.
 - __Data Analytics:__ Offers insights into key performance indicators (KPIs) and trends to support data-driven decision-making and strategic planning.


## Technologies Used

 - __Java SE (Standard Edition)__
 - __JDBC (Java Database Connectivity)__
 - __Swing (Graphical User Interface Toolkit)__
 - __AWT (Abstract Window Toolkit)__


## Setup and Installation

#### Clone the Repository:
 - Clone this repository to your local machine using Git:
 - git clone 
```https://github.com/your-username/medical-management-system.git```

#### Import Project: 
 - Import the project into your preferred Java IDE (Integrated Development Environment), IntelliJ IDEA.

#### Database Configuration: 
 - Configure the database connection parameters in the DatabaseManager.java file. Update the JDBC URL, username, and password according to your database setup.

#### Database Setup: 
 - Create a database named medical_management in your preferred RDBMS (Relational Database Management System) such as MySQL, PostgreSQL, or SQLite. Use the provided SQL script database_script.sql to create the necessary tables and schema.

#### Run Application: 
 - Compile and run the Login.java file to start the application.


## Usage

 1. Upon launching the application, the user interface will display options to manage patients, appointments, medical staff, billing, and reporting.
 2. Choose the desired operation by clicking on the corresponding button.
 3. Follow the on-screen instructions to complete the chosen operation.
 4. All changes made to patient records, appointments, medical staff, and billing information will be reflected in the database.


## DATABASE
~~~
CREATE database hospital_table;
use hospital_table;
CREATE table login(username varchar(20), password varchar(20));
select * from login;

insert into login values ('rahul','7654321');
insert into login values ('aum','tuvwxyz');
select * from login;

use hospital_table;
CREATE table patient_info(
  ID varchar(20), 
  Number varchar(20), 
  Name varchar(20), 
  Gender varchar(20), 
  Patient_Disease varchar(20), 
  Room_Number varchar(20), 
  Time varchar(100), 
  Deposite varchar(20)
);
select * from patient_info;

use hospital_table;
CREATE table Room(
  room_no varchar(20), 
  Availability varchar(20), 
  Price varchar(20), 
  Room_type varchar(100)
);
select * from Room;

insert into Room values("100","Availabil","500","G Bed 1");
insert into Room values("101","Availabil","500","G Bed 2");
insert into Room values("102","Availabil","500","G Bed 3");
insert into Room values("103","Availabil","500","G Bed 4");
insert into Room values("200","Availabil","1500","Private Room");
insert into Room values("201","Availabil","1500","Private Room");
insert into Room values("202","Availabil","1500","Private Room");
insert into Room values("203","Availabil","1500","Private Room");
insert into Room values("300","Availabil","3500","ICU Bed 1");
insert into Room values("301","Availabil","3500","ICU Bed 2");
insert into Room values("302","Availabil","3500","ICU Bed 3");
insert into Room values("303","Availabil","3500","ICU Bed 4");
insert into Room values("304","Availabil","3500","ICU Bed 5");
insert into Room values("305","Availabil","3500","ICU Bed 6");
select * from Room;

use hospital_table;
CREATE table department(
  Department varchar(100), 
  Phone_no varchar(20)
);
select * from department;

insert into department values("Surgical department","123456789");
insert into department values("Nursind department","123456789");
insert into department values("Operation theater complex (OT)","123456789");
insert into department values("Paramedical department","123456789");
select * from department;

use hospital_table;
create table EMP_INFO(
  Name varchar(20), Age varchar(20), 
  Phone_Number varchar(20), 
  salary varchar(20), 
  Gmail varchar(20), 
  Aadhar_Number varchar(20)
);
select * from EMP_INFO;

insert into EMP_INFO values(
  "Doc 1","30","0123456789", "500000", "doc1@gmail.com", "9876543234567"
);
insert into EMP_INFO values(
  "Doc 2","40","2345678901", "00000", "doc2@gmail.com", "543234567"
);
select * from EMP_INFO;

use hospital_table;
create table Ambulance(
  Name varchar(20), 
  Gender varchar(20), 
  Car_name varchar(20), 
  Available varchar(20), 
  Location varchar(20)
);

insert into Ambulance values(
  'Rahul', 'Male', '108', 'Available', 'Sector 18'
);
select * from Ambulance;
~~~