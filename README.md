# Britc POS
## An intuitive &amp; modern web based POS system

<br/>
<br/>


britc Point Of Sale
<br/>
<br/>

> Contact me for support or with ideas to make this project better. :sunglasses: :fire: :v:

<br/>
<br/>
<br/>
<br/>

#### Cashier Dashboard
![Screenshot](assets/images/CashierScreenshot.png)

***

#### Admin Dashboard
![Screenshot](assets/images/AdminDashboardScreenshot.png)


***

## Installation on Windows

  Requirement  
- Xampp for windows
- Node.js
- Git for Windows
- Que POS App folder
- Webprint - allows you to easily print from the browser. Download and install the webprint [here](https://www.ej-technologies.com/download/install4j/files).

### NOTE:
1. The guide is to be used on any edition of Windows 7 or higher 32 & 64 bits.
2. When installing Node on the machine ensure that you have added the executable to the [System Environment Variables.](https://www.tutorialspoint.com/nodejs/nodejs_environment_setup.htm)

### 1. Installing XAMPP
  Download and install XAMPP
### 2. Installing Node.js
  1. Run the nodejs installer and follow all the steps.
  2. Test if node is added to the System Environment Variable, open the terminal and run the following commands. **node -v** , this should show you the node version and **npm -v** to show the npm version.
### 2. Installing Git
  1. Run the Git installer and follow all the steps.
### 3. Installing the POS
1. Clone the application
 
![The htdocs content](https://d2mxuefqeaa7sj.cloudfront.net/s_A1859D6598480832CC3A69D343D349069DED4660B00B2771E2605A3493AA4DAD_1506356338160_Screenshot_20170925_191403.png)
![pos folder content](https://d2mxuefqeaa7sj.cloudfront.net/s_A1859D6598480832CC3A69D343D349069DED4660B00B2771E2605A3493AA4DAD_1506356364973_Screenshot_20170925_191443.png)

2. Install dependencies. To do that, open your terminal, cmd or GIT bash should be okay, navigate to the **pos** folder and run the following command, **npm install socket.io**  
3. Enable apache modules and adjust the root folder. Now open httpd.conf and search for the following lines:
    To open httpd.conf click **config** button that’s highlighted below.
![](https://d2mxuefqeaa7sj.cloudfront.net/s_A1859D6598480832CC3A69D343D349069DED4660B00B2771E2605A3493AA4DAD_1506356567616_Screenshot_20170925_191236.png)
  
    `proxy_wstunnel` and uncomment the line by removing the # symbol at the start of the line.
![enabling the proxy module](https://d2mxuefqeaa7sj.cloudfront.net/s_A1859D6598480832CC3A69D343D349069DED4660B00B2771E2605A3493AA4DAD_1506356300661_Screenshot_20170925_191627.png)

    `DOCUMENTROOT` and adjust it as shown in the image below, to point to the pos folder, ie `C:/xampp/htdocs/pos`.
![setting the document root](https://d2mxuefqeaa7sj.cloudfront.net/s_A1859D6598480832CC3A69D343D349069DED4660B00B2771E2605A3493AA4DAD_1506356280127_Screenshot_20170925_191656.png)

  Restart apache server to apply the changes, clicking the stop button and then clicking the start button again. Now go to your browser to set-up the application for the first time.


- Navigate to [localhost](http://localhost/installer) and follow the steps. Under requirements for the application, if you followed carefully, should have all of them checked except https active , which we only need if we have to go live and Application folder shouldn’t be writable, which doesn’t apply in windows environment. To proceed that way check the last item on the list and the next button will activate, then click it.
- Open another tab and navigate to [PHPMYADMIN](http://localhost/phpmyadmin) and create an new database to be used by the pos.The name of the database will be required during the installation. Now go back to the installer and fill in your mysql database credentials on the form, the database name will be the name you gave to your database. If you have not changed any settings for MySql, your host - **127.0.0.1** , **port** **3306** , **username** - **root** , **password** - (nothing -leave it blank) which are the default login credentials.
- Set any other required information till the end. Login and go to admin and Settings and set them to your liking.

***
