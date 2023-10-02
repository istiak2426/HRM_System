
### **_Human Resource Management_** System Using Node.js and MySQL


## Create / Select MySQL Database

```
CREATE DATABASE databasename;
USE databasename;
```

## Create employees Table

```
CREATE TABLE employees (
  id INT NOT NULL,
  firstName VARCHAR(255) NULL,
  lastName VARCHAR(255) NULL,
  age INT NULL,
  sex VARCHAR(1) NULL,
  phoneNumber VARCHAR(255) NULL,
  PRIMARY KEY (id)
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
