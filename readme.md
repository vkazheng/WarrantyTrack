# WarrantyTrack

PHP application for business owners who are looking for customers inquiries software.
At a shop I'm working at, we are using very bad customers inquiries software, I decided to make a better one 😛.

In this application you as the store owner (or your employees), can open inquiry cases for defective products brought by customers in order to track the status of the inquiry..

I developed this project mainly to see if I can build (and finish) a full working project, and to provide a fully working product for your business.

If you are a developer,
Feel free to contribute to this project.

## Installation:

1. Fork the project and upload it to your Apache/Ngix server.
2. Import the included MySql DB. 
3. Adjust the API/sqlog.php file to point to your DB.
4. Your first time authentication details are:
  ```
  admin
  1234
  ``` 
5. Login to the panel and adjust the Settings.
6. You are all set.


## Demo

You can test the project [here](http://api.noamsapir.me/Experiments/WarrantyTrack/):

Login:
```
  worldwideweb
  1234
```

## TODO:
- ~~Search cases~~
- Admin panel
  - Redesign form submitaion
  - Detailed reports page
- Auto installer
- Redesign code
- SMS/ Email system.

## NOTE:
Error:
Uncaught Error: Call to undefined function mysqli_fetch_all() in Domain/panel.php:17

Issue seems to be 'mysqli' and 'mysqlnd' are not working together. I had the same issue in cpanel

Steps:
1) Go to CPanel dashboard
2) Go to 'Select PHP Version', you should see a bunch of checkboxes
3) Set PHP version (5.4 or above)
4) Uncheck the 'mysqli' extension and check both 'mysqlind' and 'nd_mysqli'

Apparently 'nd_mysqli' is 'mysqli' but configured to work with 'mysqlind' and to make it work you have to uncheck 'mysqli' due to settings conflicts.
