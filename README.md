# IoT Project: Live Weather Station -Python, PHP, RaspberryPi, SenseHat's Weather sensors
An IoT project to send live local weather data gathered using Raspberry Pi's SenseHat to a remote database and display in an online dashboard at www.math.foodonya.com/iot Stack used: Python, Python external libraries, PHP, MySQL, Apache, Bootstrap, CSS, jQuery. This public repository must be used for non-commercial educational use only.

## Dashboard

![Image of Dashboard](https://math.foodonya.com/iot/r_admin_use/dash_img.jpg)

## Getting Started

Clone this public repo to your local machine for your development and testing purposes.

### Prerequisites

* **Some coding experience essential.**
* [XAMPP](https://www.apachefriends.org/index.html) - Local web server. [PHP](https://www.php.net/) comes with it.
* [MySQL Workbench](https://www.mysql.com/products/workbench/) - Local database server.
* Any code editor. I used [VS Code](https://code.visualstudio.com/).
* [Python](https://www.python.org/) - Latest version (or must be above 3.5).
* A web hosting account that supports PHP and MySQL.
* [Raspberry Pi](https://www.raspberrypi.org/) or similar.
* [Sense Hat](https://www.raspberrypi.org/products/sense-hat/) or similar.
* A Mac or PC for PHP, MySQL development. Python development can be done in Pi.
* [Git](https://git-scm.com/) of course, to clone this project.


## How this project works?
1. Python collects the SenseHat sensors' data and sends the data using POST request to the data_collector.php file in webserver.
2. Data_collector.php is a backend file that writes the received data into a MySQL database, whenever a POST request is received.
3. Iot_dashboard.php is the frontend file that periodically gets new data from the MySQL database and displays it in a dashboard. Iot_dashboard_tiles.php and conn_php_math_db.php are its helper files. Iot_dashboard.php is the file users will visit to see the weather data.
4. Db_cleaner.php is for cleaning up the database once in a while to keep the database size smaller. This file works similar to Data_collector.php.
5. IoT device's exception errors are collected and logged into error.log file for troubleshooting.


## Where do these files run?

### While in Local development

* PHP files will be served by your XAMPP local server.
* MySQL Database will be hosted in a live webserver's [cPanel](https://www.cpanel.net/) > [phpMyAdmin](https://www.phpmyadmin.net/)
* MySQL Workbench serves this database locally for development.
* Python script runs in your IoT device. This was a Raspberry Pi connected with a SenseHat in my case.

### While in Production

* PHP files live in your [webserver](https://math.foodonya.com/iot/php/iot_dashboard.php)
* MySQL Database will be hosted in your webserver's [cPanel](https://www.cpanel.net/) > [phpMyAdmin](https://www.phpmyadmin.net/)
* Python script runs in your IoT device. This was a Raspberry Pi connected with a SenseHat in my case.

## Deployment (out-of-scope)

Explaining deployment of this repo / project in both local and production environments is out-of-scope of this Readme page. However, there are plenty of resources available online posted by talented and generous IT community all around the world. Also, lots of comments were added through-out the code files for reading and understanding what is going on. 

## License

This public repository can be used for non-commercial and educational use only.

## Authors

* **Raja Palanivel** - *PHP, Python, MySQL, Bootstrap, CSS, jQuery, Git* - Another project here: [Foodonya.com](https://foodonya.com/)
* **Yavany Arumuga Raja** - *HTML, Bootstrap, CSS, Python* - Year 7 Student.

## Acknowledgements

* Hats off to anyone whose Python libraries were used in this project.
* Inspirations by friends, [Bala](https://www.linkedin.com/in/balasmn/), [Prashanth](https://www.linkedin.com/in/prashanth-umashanker-a28a6019/).
* The Open source community
