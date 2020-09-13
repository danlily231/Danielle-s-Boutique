# Danielle's Boutique
I. Overview

Here is a new online clothes store name “Danielle's Boutique” where users can purchase clothes of their choice. The main idea of our website is to allow users from all around the USA to buy all types of clothes on our website with convenient checkout options.
The website will be similar to Hollister, a well-known in-store and online clothing purchasing site, but we strive to offer clothes at a better price and an easy checkout option. We constructed the website with multiple views, where the admin view gets the opportunity to add and or remove clothes from the database. Additionally the administrator can alter the inventory count of the clothes on the database. Both of these functionalities will be conveniently available through the website and thus our website gives the user a seemingly user-friendly environment.

II. Database Design

The following ER diagram provides a high-level introduction to our database. This will be helpful to understand the relation between the tables. (Only Ships to U.S.)

III. Client Functionality

Every page will have a menu bar at the top of the website. This will help all types of users to move around the website with aese. There is also a section, at the bottom of each page, where the contact information, both phone number and email address is provided. Also, credit is given to w3.css for providing the template for the website.
   
1. Guest User

If the user is not logged in, the menu bar will consist of four different options of “Home Page”, “Shopping Cart”, “Create Account” and “Login”.

a. Home Page
The home page is the first page users can see when they connect to the website. The home page will have the most trending collection’s name and it’s pictures. Also, the most best selling clothes will be displayed on the home page with the prices. The top clothes keep changing as the number of purchases for each garment changes.
The home page will also consist of the shop by Category section. This section will have six different types of options. Each option will take the user to the different page, where they will be able to view more clothes under that specific category. Clicking on the home page button, the user will be brought back to the home page view.
Guest users can see the option to purchase on the home page, and they will still be able to purchase clothes. The log out page is simply for the logged in user to log out the website once they finish visiting the website.
The application layer will check if the user is logged in or not. If so, the section will get closed and the user will be logged out and directly to the home page of the guest user.
The application layer is implemented by HTML, CSS and PHP.

b. Shopping Cart
The shopping cart will contain all of the items that the user has selected from the website.
They will be able to adjust the quantity of items in their cart as well as remove items from it.
They will then be able to proceed to the checkout and purchase their items.

c. Create Account
The Create Account page will ask the user to enter their personal information as well as the password they would like to use for security purposes.
It will ask them their first name, last name, address, email address, password, address, zip code, and state.
Once all the information is entered the user will click the submit button and their account will be created.

d. Login

2. Account User

The login page will be for the user with an existing account. Here the user will ask to input their user name in the form of email and password attached to that account.
Similar to the New user page, if there is a missing information detected then the error message will pop up.
The application layer will query the database with the information the user provides. If the information is valid for a user in the database then it will log that user in.
Additionally, if a user tries to login with a username not present in the user table, the application layer will query the database and look for that username if not present in the table, the application layer will return the error message on the client side.
Once the user is logged in, the menu bar will consist of the four options: “Home Page”, “Shopping Cart”, “Create Account”, and “Logout”

a. Home Page

 The home page function is the same as mentioned above in the guest user section above.
When the user is logged in, they can purchase the clothes they like. They can also input the number of clothes they would like to purchase and add them in their shopping cart.
The same function for adding the clothes to the shopping cart is applied to all the clothes which users see in the shop by category section.
The application layer will invoke the shopping cart php file, which will query the database and get the cloth id which was selected by the client. Meanwhile the shopping cart will be updated and displayed on the client sides.

b. Shopping Cart
The shopping cart is a temporary state page that shows the user which items they have added to their order during their current visit to the website.
The users can change their shopping cart by both modifying the quantities of clothes in their cart when by add the clothes to shopping cart, as well as deleting clothes from their cart.
The users will be able to view the total price of their order.
When the user click on purchase button, they will be transfer to order page.
The user is supposed to enter their details, such as email, first name, last name, address and credit card number. Once hit the submit they will be provided a confirmation number which will be unique for each purchase order.

c. Login
The user will click the button on the menu bar on the home page and be brought to this page where they will be prompted to enter the email address and password associated with their account.
There will also be a button below offering them the chance to create an account.
Once the user has entered their information into the email and password boxes they will click submit and be brought to the home page.

d. Logout

3. Admin

a. Login
This will be a clickable button on the menu bar that will logout the user when clicked and take them back to the home page.
The user will click the button on the menu bar on the home page and be brought to this page where they will be prompted to enter the email address and password associated with their account.
There will also be a button below offering them the chance to create an account.
Once the user has entered their information into the email and password boxes they will click submit and be brought to the home page.

b. Home Page
In the admin page, the admin can see top collections and look around the website mostly the same as a user except the admin will have several options a normal user does not have.
The admin will have access to add clothes, change prices, change stock, delete clothes and update clothing quantity.

The application layer will query the database with the manager’s email and password. If successful, the user will be detected to admin view.
Here the user will not be able to buy any clothes.

c. Add Clothes
The page will require the admin to insert the clothing name, clothing type, clothing year released, the name of the clothing designer, the clothing’s price and the stock quantity.
When the admin clicks on add cloth the application layer will use the information inserted and update the clothing table with it.
When the update is successful the admin will be notified by a message.

d. Change Price
This page will require the admin to input the cloth ID, cloth name and new price.
The application layer will query the database with the inserted cloth ID and cloth name. If matched with any existing clothes in the cloth table then the price for that cloth will be changed in the database.

e. Change Stock
This page will require the admin to input the cloth ID, cloth name and new stock for that cloth.
The application layer will query the database with the inserted clothing ID and clothing name. If matched with any existing clothes in the cloth table then the stock number entered will be added to the existing stock number in the database.

f. Delete Clothes
Only the admin can view this page.

IV.
This page will display the item’s picture and information with a red button at the bottom of the page that says “Delete Item”.
Once the button is clicked, the application layer will clear the item’s information from the database.
When the update is successful the admin will be notified by message.
Log Out
This will be a clickable button on the menu bar that will logout the user when clicked and take them back to the home page.
