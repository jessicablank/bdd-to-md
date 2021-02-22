# Invoice list view
Invoice list view is presentation of all customer's invoices in one view.
From invoice list view, customer may select a sepcific invoice for viewing.


**Assuming following conditions apply**
* Given  User is logged in


## Scenario: User can view customer's invoices if the user has privileges
* Given  Bob Sponge has privileges for a customer
* When  Bob Sponge opens the invoice list view
* Then  He sees the invoices of the customer


## Scenario: Admin user can view invoices of all customers
* Given  Largo Notsogrande has admin privileges
* When  Largo Notsogrande opens the invoice list view
* Then  He sees all invoices
# Login
Login view enables registered users to login to system.
If unauthorized user tries to login, guiding error messages are displayed accordingly.


## Scenario: Logging in with valid user name and password
* Given  That valid user inputs name and correct password, longer than 8 characters
* When  User clicks the login button
* Then  The user is redirected to invoice list view


## Scenario: Logging in with invalid user name
* Given  That invalid user name is input to the user name field
* When  User clicks the login button
* Then  An error message is shown indicating the login failed


## Scenario: Logging in with invalid password
* Given  That invalid password is input to the password field
* When  User clicks the login button
* Then  An error message is shown indicating the login failed