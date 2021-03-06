#Week of 14 Homework Node Express Handlebars
_______________________________________________________

In this assignment, you'll create a burger logger with MySQL, Node, Express, Handlebars and a homemade ORM (yum!). Be sure to follow the MVC design pattern; use Node and MySQL to query and route data in your app, and Handlebars to generate your HTML.

You will be fully capable of doing this homework by the end of Saturday's class.
_______________________________________________________

### Before You Begin

* Eat-Da-Burger! is a restaurant app that lets users input the names of burgers they'd like to eat.

* Whenever a user submits a burger's name, your app will display the burger on the left side of the page -- waiting to be devoured.

* Each burger in the waiting area also has a `Devour it!` button. When the user clicks it, the burger will move to the right side of the page.

* Your app will store every burger in a database, whether devoured or not.

* [Check out this video of the app for a run-through of how it works](burger_demo.mp4).
_______________________________________________________

## Instructions - ALL INSTRUCTIONS REMAINING AS OF 12:25 PM 2/9/2017 HAVE BEEN ADDED TO THEIR RESPECTIVE FILES AND LEFT BELOW FOR REFERENCE.
_______________________________________________________

#### App Setup
APP SETUP COMPLETE
_______________________________________________________

#### DB Setup:

2. In `schema.sql`, write SQL queries this file that do the following:
	* Create the `burgers_db`.
	* Switch to or use the `burgers_db`.
	* Create a `burgers` table with these fields:
		* **id**: an auto incrementing int that serves as the primary key.
		* **burger_name**: a string.
		* **devoured**: a boolean.
		* **date**: a TIMESTAMP.

4. In `seeds.sql`, write insert queries to populate the `burgers` table with at least three entries.

7. Run the `schema.sql` and `seeds.sql` files into the mysql server from the command line

8. Now you're going to run these SQL files. 
	* Make sure you're in the `db` folder of your app.

	* Start MySQL command line tool and login: `mysql -u root -p`.

	* With the `mysql>` command line tool running, enter the command `source schema.sql`. This will run your schema file and all of the queries in it -- in other words, you'll be creating your database.

	* Now insert the entries you defined in `seeds.sql` by running the file: `source seeds.sql`.

	*
	 Close out of the MySQL command line tool: `exit`.
_______________________________________________________

#### Config Setup:

2. 
	* Inside the `connection.js` file, setup the code to connect Node to MySQL.

	* Export the connection.

3.
	* Import (require) `connection.js` into `orm.js`

	* In the `orm.js` file, create the methods that will execute the necessary MySQL commands in the controllers. These are the methods you will need to use in order to retrieve and store data in your database.
		* `selectAll()` 
		* `insertOne()` 
		* `updateOne()` 

	* Export the ORM object in `module.exports`.
_______________________________________________________

#### Model setup:

* Inside `burger.js`, import `orm.js` into `burger.js`

	* Also inside `burger.js`, create the code that will call the ORM functions using burger specific input for the ORM.

	* Export at the end of the `burger.js` file.
_______________________________________________________

#### Controller setup:

3. Inside the `burgers_controller.js` file, import the following:
	* Express
	* `burger.js`

4. Create the `router` for the app, and export the `router` at the end of your file.
_______________________________________________________

#### View setup:

* Setup the `main.handlebars` file so it's able to be used by Handlebars.

* Setup the `index.handlebars` to have the template that Handlebars can render onto.

* Create a button in `index.handlebars` that will submit the user input into the database.
_______________________________________________________

#### Directory structure:
DIRECTORY STRUCTURE CREATED