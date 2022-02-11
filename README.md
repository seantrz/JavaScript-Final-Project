# JavaScript-Final-Project

Step 1
Create an Express application with the Express generator

This application should be named L10HandsOn and should live within your Express-Course directory
Install all needed dependencies
This application should use Sequelize as its ORM

Step 2
Create a new MySQL database called bulletinboard

Step 3
Run migrations to create two new tables: users and posts

These tables should have the following structure:
users:
UserId: integer, autoincrement, primary key, not null
FirstName: string
LastName: string
Username: string, unique
Password: string
Email: string, unique
Admin: boolean, default value is false, not null
createdAt: date, not null
updatedAt: date, not null
posts:
PostId: integer, autoincrement, primary key, not null
PostTitle: string
PostBody: string
UserId: integer, foreign key to UserId in users table
createdAt: date, not null
updatedAt: date, not null

Step 4
Update models to reflect the create table migrations

Don't forget the associations
Step 5
Users should be able to Signup/Login/Logout
Use JWT for secure login (hashing and salting passwords)

Step 6

Users should be able to create, edit, and delete
Be able to click on a post to update or delete it
Run a migration to add a Deleted column
After the post has been deleted, redirect the user to their profile page

Step 7
Users should be able to view their profile page. Their profile page should render the following:
Their full name
Their username
The posts they have written

Step 8
Admin users should be able to see a list of all users that have not been deleted by the user's first and last name
Run another migration to add a Deleted column
Render a different hbs file for the Admin profile page, which should list all users
Every Admin should see the same page. Use the route /users/admin

Step 9
Admin users should be able to click on a user and view their information, but not edit their information
Use the route /users/admin/editUser/:id

Step 10
Admin users should be able to Delete users and their posts, but not edit them

Step 11
Add some styling to your application so it is unique to your taste
