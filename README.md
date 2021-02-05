# Open-Data-Interface-for-Schools
Open science and as part of it, open data has the potential to bring transparency and scientific innovation. With the availability of openly accessible datasets, students could have the opportunity to work with real datasets e.g., about their city or neighborhood, and understand different facts and real-life problems at a local level. To facilitate teachers and students an open data interface develpoed using open source tools that provides direct access to educational datasets categorized under the educational domain: science, math, and geography. 
# Get Started
As a first step, design and test WordPress website on localhost. Install WordPress & XAMPP.
## XAMPP Installation
Download XAMPP for windows from apachefriends.org and install. Then, run the installer to get start with the XAMPP setup. In the component wizard, all the components are by default selected. You can uncheck the components that you don’t plan to use. We have chosen the Apache, MySQL, PHP and phpMyAdmin since these are necessarily required for WordPress installation. 
# Install
Chose the Apache, MySQL, PHP and phpMyAdmin components in setup wizard and specify the location for where to install XAMPP.
Open XAMPP control panel,default location of XAMPP folder is  C:\xampp. Start the Apache and MySQL components. Open  phpmyadmin from http://localhost/phpmyadmin .
# WordPress Installation
On phpMyAdmin interface, create the database.
After creating the database, we are set to start the installation of WordPress. Download WordPress. WordPress can either be used online at www.wordpress.com or accessed as a downloadable version at www.wordpress.org. Once the download is complete, extract the zip file to C:\xampp\htdocs\. If you’ve extracted the package correctly, you will see the “wordpress” folder inside htdocs. Select language. Set the title of site and fill up user information, like site title, username, password and Email. Fill up the required fields, and press “Install WordPress”. Choose theme Hastia and make respective pages for your interface and test its features  on your computer.
# Install Visualization tool
We use Tableau as a visualization tool. Install Tableau https://www.tableau.com/ and make visualizations of the open datasets to be included on your web interface. Once the visualizations are ready, embed visualization code on the respective WordPress pages and test all the features locally.
# Move WordPress from Localhost to Live Server
 To move your WordPress site manually, you will first export it via phpMyAdmin.
# Step 1: Export Local WordPress Database
Navigate to http://localhost/phpmyadmin/ and select WordPress database and click on Export at the top of the phpMyAdmin window. The “Quick” export method is selected by default. Leave it and click Go. A SQL file (such as my_test.sql) will be exported to the downloads folder on your computer.
# Step 2: Upload WordPress Files to Live Site
 Using FileZilla FTP client upload wrdpress files to live server. Connect to web hosting account and browse the root directory of live server. Upload all the files in the right destination directory. 
#  Step 3: Create New Database on Live Site
Navigate to phpMyAdmin thorugh localhost/phpmyadmin and select MySQL Databases. Create a database and specify name. Next navigate to the MySQL Users section. Here, create or add an existing user to the database.
# Step 4: Import Local Database on Live Site
Navigate to phpMyAdmin. Now, you can see your newly created database in phpMyAdmin. Go to Import page by clicking the Import Tab on the top bar menu. Next, click on Browse button to choose the database file created in step 1. Then, press Go to import your WordPress database.
# Step 5: Redirect the Site URLs
Finally replace all the links in the database that point to the old site location. 
# Step 6: Set Up Your Live Site
Once you import the database, it’s time to configure wp-config.php. Connect to your website using an FTP client, find wp-config.php file and right click to View/Edit. Look for the information:Provide the database name, user, and password you created in the earlier step. After that, save the wp-config.php file and upload it back to your server. 

define(‘DB_NAME’, ‘your_database_name’);

define(‘DB_USER’, ‘your_database_user’);

define(‘DB_PASSWORD’, ‘your_database_password’);

define(‘DB_HOST’, ‘localhost’);

Open data interface is ready to go.
