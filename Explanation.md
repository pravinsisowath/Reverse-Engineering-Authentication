1. server.js
Requires npm packages (express, express-session, passport) to create a server, a user session, and an authenticated login. var PORT says to use any port available and if there aren't any available then to use 8080. var db brings in the exported models created in the models folder. var app is created and utilizes express. Following this, middleware is created linking urlencoded, json, and the public folder. Passport is then used to keep track of the user's login. Routes are then brought in that were created in the routes folder (login, signup, and members). The database is then synced and a message is displayed if successful.

2. Routes
a. api-routes.js
Import models and passport. Uses passport to authenticate and validate a user's login info and bring them to the members page, and if not then user will be sent back an error. Route is made to sign up a user and store their password securely. Another route is created to also log a user out. Final route is created to get user's data to be used client side.
b. html-routes.js
Path is imported to use relative routes to HTML files. Uses middleware to check if authenticated and keeps user logged in if so. Routes are created to either send users to members page or redirect to the signup page.

