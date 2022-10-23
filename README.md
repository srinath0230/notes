# CS50 Final Project - website Web application

The project is a webpage where teachers can create assignments for students. The implementation is fairly simple, to keep the project scope in check. I wanted to make a project like this to expand my knowledge of Node JS and of techniques like buffer piping from database to client, role based authentications, etc.

Technologies used:

- Python
- SQL
- JavaScript
- CSS
- HTML
- Bootstrap
- other small libraries or packages

## How the webpage works?

The idea is simple. The user can register using email and firstname. During registration you need to enter these fields:

- Email
- Name
- Password: it is checked to match, must be at least 6 symbols long and is hashed after checks are done


Registration allows you to access  dashboard, where you can see created Notes. either you can copy paste. Once the notes submission it will appear instead of <input type="file">.



### Routing

Each route checks if the user is authenticated. It means if correct mail and password were supplied and what role it has. No one can enter into another person account.

### Sessions

The webpage uses sessions to confirm that user is registered. Once the user logins, his credentials are checked with (werkzeug.security) library. Once everything passes a session is created and stored in the cookies. The server attaches user to subsequent requests, so the back-end can easily access the details, like

### Database

Database stores all users, there personal information. The tables, like Users submissions uses foreign keys to relate users to submitted Notes.

## Possible improvements

As all applications this one can also be improved. Possible improvements:

- Have administrator account which confirms user identity, so that there will be no spam notes could not register twice
- Ability to change account details
- Have a way for person to upload videos.
- Notificaitons when someone you follow upload a video or notes.

## How to launch application

1. Check that you have Node version 8+
2. Clone the code: `git clone https://github.com/me50/srinath0230.git`
3. Run command prompt in the folder and run `pip install -r requirements.txt` to install all dependencies
4. In your browser go to `localhost:5000`
5. You are ready to go!

## About Flask

Flask is a micro web framework written in Python. It is classified as a microframework because it does not require particular tools or libraries. It has no database abstraction layer, form validation, or any other components where pre-existing third-party libraries provide common functions.

- You can download flask web framework by <b>pip install flask</b>

## About SQLALCHEMY
SQL databases behave less like object collections the more size and performance start to matter; object collections behave less like tables and rows the more abstraction starts to matter. SQLAlchemy aims to accommodate both of these principles.

SQLAlchemy considers the database to be a relational algebra engine, not just a collection of tables. Rows can be selected from not only tables but also joins and other select statements; any of these units can be composed into a larger structure. SQLAlchemy's expression language builds on this concept from its core.

SQLAlchemy is most famous for its object-relational mapper (ORM), an optional component that provides the data mapper pattern, where classes can be mapped to the database in open ended, multiple ways - allowing the object model and database schema to develop in a cleanly decoupled way from the beginning.

SQLAlchemy's overall approach to these problems is entirely different from that of most other SQL / ORM tools, rooted in a so-called complimentarity- oriented approach; instead of hiding away SQL and object relational details behind a wall of automation, all processes are fully exposed within a series of composable, transparent tools. The library takes on the job of automating redundant tasks while the developer remains in control of how the database is organized and how SQL is constructed.
