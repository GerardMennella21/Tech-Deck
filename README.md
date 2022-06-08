Tech-Deck by Gerard Mennella

# Summary
This application is a CMS style tech blog allowing users to create an account, create posts, and like or comment on posts. All posts are viewable on the homepage and the dashboard shows the logged in user's posts and allows them to edit or delete them.

# Code Breakdown
## Tests
The helpers test ensures the functions in the helpers file in the utils folder are successful.

## Config
The connection file sets up the sequelize connection to either the jawsDb or localhost.

## Controllers
The api folder contains the routes for the comment, post, and user data. The index joins and exports them. The dashboard and home routes are directly in the controllers folder to be used on the front-end at different url endpoints. They are joined and exported by the index.

## db
The schema creates the tech_deck_db database

## Models
Contains the models for Comment, Post, User, and Vote. The index defines their relationships and exports them.

## public/javascript
Contains the front-end javascript functions needed for the application. There are functions to signup & login/logout that interact with the users table. There are functions to add, edit and delete posts also using fetch requests. The last two functions are to create comments and like posts.

## Utils
Contains the helpers and withAuth functions. The helpers are formatting tools and the withAuth ensures users have authorization to perform certain actions by user id.

## Views
The views folder contains the main layout, page structures, and partials for comments and posts. api data is inserted accordingly using handlebars syntax and the pages are styled using bootstrap.

## Server
Creates the server using express and syncs to the sequelize connection. The session is also defined and used by express with a logout after 30 minutes of inactivity.

# Screenshots
![Screenshot](./screenshots/homeScrnsht.png)

# Deployed Application
https://stormy-lowlands-21347.herokuapp.com/