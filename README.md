This project will contain brushup of Web Development.

Development Environment:

1) OS - Linux (Ubuntu 12.04) </br>
2) Local server - Apache (apache2)


<b>Install Apache in Ubuntu:</b>

Disclaimer: The below instructions are for Ubuntu 12.04, might change slightly for other versions of Ubuntu.

Open your terminal and type the following command:

`sudo apt-get install apache2`

Once the above command completes and you don't get any error, then open up the `http://localhost/` in any web browser of your computer. 

You should see something like <b>It Works!</b> on the webpage. If you see that, then you have successfully installed your local web server. Hurray!!


<b>Start, stop, re-start Apache</b>

Using the following commands you can start, stop or re-start your apache server whenever needed.

```
sudo /etc/init.d/apache2 start   #start apache
sudo /etc/init.d/apache2 stop   #stop apache
sudo /etc/init.d/apache2 restart   #re-start apache
```

Apache will auto-start whenever you are booting up your computer. So to prevent that you can type:

`sudo update-rc.d -f apache2 remove`

Incase, you want to restore back to autostart, type:

`sudo update-rc.d apache2 defaults`

Now, go to `/var/www` folder from your terminal. You can see `index.html` file in that folder. That `html` file is showing in your `localhost` webpage. You can create `n` number of `html` files and it will be displayed in your localhost. Example, you created `homepage.html` in your `/var/www` directory, then type `http://localhost/homepage.html` in any web browser of your computer, you can see the results.


Suppose, you want to change the directory and point your webpage to direct to some other folder, then create a folder viz. `public_html` in your `/home/username` directory. If the folder already exists then you don't need to create it. Create a file named `index.html`. Then, type the following in your terminal:

`gksu gedit /etc/apache2/sites-enabled/000-default`

This will open up a file, where you need to make the following changes:

```
Change DocumentRoot /var/www to DocumentRoot /home/user/public_html

Change <Directory /var/www/> to <Directory /home/user/public_html/>
```

Save and exit the file and restart the apache server using the above restart command. Now, go to your locahost in your web browser and you can see the contents of your new `index.html` file from your `/home/username/public_html` folder.
