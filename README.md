This project will contain brushup of Web Development.

Development Environment:

1) OS - Linux (Ubuntu 12.04)
2) Local server - Apache (apache2)


Install Apache in Ubuntu:

Disclaimer: The below instructions are for Ubuntu 12.04, might change slightly for other versions of Ubuntu.

Open your terminal and type the following command:

`sudo apt-get install apache2`

Once the above command completes and you don't get any error, then open up the `http://localhost/` in any web browser of your computer. 

You should see something like <b>It Works!</b> on the webpage. If you see that, then you have successfully installed your local web server. Hurray!!


<b>Start, stop, re-start Apache</b>

Using the following commands you can start, stop pr re-start your apache server whenever needed.

```
sudo /etc/init.d/apache2 start   #start apache
sudo /etc/init.d/apache2 stop   #stop apache
sudo /etc/init.d/apache2 restart   #restart apache
```
