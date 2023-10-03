
### **_Human Resource Management_** System Using Node.js and MySQL


## Create / Select MySQL Database

```
CREATE DATABASE databasename;
USE databasename;
```

## Create employees Table

```

-- Create the Company table
CREATE TABLE Company (
    CompanyID INT AUTO_INCREMENT PRIMARY KEY,
    CompanyName VARCHAR(255) NOT NULL,
    FoundedDate DATE,
    Address VARCHAR(255)
   
);

-- Create the Department table
CREATE TABLE Department (
    DepartmentID INT AUTO_INCREMENT PRIMARY KEY,
    CompanyID INT,
    DepartmentName VARCHAR(255) NOT NULL,
    ManagerID INT,
    FOREIGN KEY (CompanyID) REFERENCES Company(CompanyID)
 
);

-- Create the Designation table
CREATE TABLE Designation (
    DesignationID INT AUTO_INCREMENT PRIMARY KEY,
    DesignationName VARCHAR(255) NOT NULL,

);

-- Create the Employee table
CREATE TABLE Employee (
    EmployeeID INT AUTO_INCREMENT PRIMARY KEY,
    CompanyID INT,
    DepartmentID INT,
    DesignationID INT,
    FirstName VARCHAR(255) NOT NULL,
    LastName VARCHAR(255) NOT NULL,
    DateOfBirth DATE,
    FOREIGN KEY (CompanyID) REFERENCES Company(CompanyID),
    FOREIGN KEY (DepartmentID) REFERENCES Department(DepartmentID),
    FOREIGN KEY (DesignationID) REFERENCES Designation(DesignationID)
   
);

-- Create the Increment table
CREATE TABLE Increment (
    IncrementID INT AUTO_INCREMENT PRIMARY KEY,
    EmployeeID INT,
    IncrementDate DATE,
    IncrementAmount DECIMAL(10,2),
    FOREIGN KEY (EmployeeID) REFERENCES Employee(EmployeeID)

);
```

## Create `.env` File

```console
cd server
touch .env
```

#### .env file config

- HOST=_HOST_
- USER=_USER_
- PASSWORD=_PASSWORD_
- DATABASE=_DATABASE_

## Install Dependencies

```console
npm install
```

## Run the Server

#### Development Build

```console
npm run dev
```

#### Production Build

```console
npm run build
npm run preview
```
