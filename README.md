# Installation Steps

### Requirements:
* Database named: **db_health**  
* NodeJS

### Github:
Clone repo: ​[https://github.com/NDily1230/myapp](https://github.com/NDily1230/myapp)
```bash
git clone https://github.com/NDily1230/myapp
```

### Database:
1. Create a mysql database called _bd_health_
2. Go to the project folder
3. Go to the config file and open up config.json in your text editor
4. Change the development options to match your local database

### Command Line Steps:
```bash
# Navigate to the project folder
$ cd project_folder/
# Installs the node dependencies
$ npm install
# Sets up developement environmnet
$ export NODE_ENV=development
# Set up databases with Sequelize
$ sequelize db:migrate
$ sequelize db:seed:all
# You should have a companies table with data, and an empty job table in your db
# Start the server
$ npm start
```

Now go to localhost:3000 in your browser and the project should be up.

## Understanding the Project

### Routes
**(Line 7-9)**: ​​Link the files where you define your routes to your project

**(Line 23-25)**: ​​When a user visits the specified route use the files defined in lines 7-9
  > Ex: When you visit localhost:3000/users the app will do whatever it is told to do within the routes/users.js file
1. To create a new base route such as localhost:3000/account, you could create an account.js file inside the routes folder and then link to it in app.js
2. To create a route such as localhost:3000/users/status you could create a new handler in the users.js file inside the routes folder

### Views
You have a basic pug template loaded with bootstrap inside the views folder
* **Layout.pug** contains the nav bar and sidebar
  * `block content` is where you can load dynamic views into
* **index.pug** extends the layout and adds to `block content`
  * to create new views inside the layout you would structure them like
index.pug

### Sequelize
Used to work with your MySQL database (create, delete tables, manipulate data)  
All information found here: ​[Sequelize Docs](http://docs.sequelizejs.com/)

