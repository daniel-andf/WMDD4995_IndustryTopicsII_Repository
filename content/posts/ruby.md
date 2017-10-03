---
title: "Ruby"
date: 2017-10-01T17:23:16-07:00
draft: true
---



<h2><strong>Introduction </strong></h2>

Ruby on Rails is being used for some of most of revelant companies in the world, such as Git Hub, AirBnb, Groupon, Hulu, etc.
In addition, there is a hign demand for Ruby on Rails on the labour market for web back-ending development. 
However, there are some languages in the market where you must take into account, before considering to use Ruby in your project.


Here are some Advantages and Disadvantages of developing on Ruby on Rails :

<h3><strong>Advantages</strong></h3>

- Uses MVC(model-view-controller) philosophy, in order to separate the application in models, which is easier for developers to add new features and maintainace.

- You don't need to code all your applications from scratch. You can use RubyGems to install some feature in your website that was already developed before.

- Language and Gems are well documented online.

{{< figure src="/img/img23.png" title="MVC-Ruby" >}}


<h3> <strong> Disadvantages </strong></h3>

- Lower performance, mainly, because of use of great amount of gems.

- Less popular than Java and PHP, therefore, there are less developers than these languages.


<h2> <strong>Basic Concepts </strong></h2>

This post will show how you prepare your machine to start developing using Ruby on Rails. 

Before we start to prepare a development enviroment for Ruby on Rails, there are a few concepts that we should know :

- <strong> Ruby </strong>- Created by Yukihiro Matsumoto, Ruby is the programming language used to code. Ruby is a language used for general purposes, not only for web development.

- <strong> Ruby on Rails </strong> -  is a web application development framework written in the Ruby language. It is designed to make programming web applications easier by making assumptions 
about what every developer needs to get started.(add citation)

- <strong> Gem (RubyGems) </strong>- is the package manager for the Ruby programing language that provides lots of libraries to your Ruby project. Before you start, it is recommended to check the RubyGems website,
to check if the features you want to use on your project is already available.

- <strong> IRB (Interactive Ruby Shell) </strong> - is the command line interface with Ruby, which allows to interact with code, when it is running.

<h2> <strong> How to install Ruby on Windows and Mac </strong> </h2>

There are a few differences on installing Ruby on Windows and Mac PCs. MacOs after version 10.12 already have Ruby installed, so you will just need to check the version of Ruby on this machine.

{{< figure src="/img/img17.png" title="Ruby on Mac" >}}

<h3> <strong> Step 1 - Install RubyInstaller (Windows only) </strong> </h3>

If you don't have the Ruby installed on your machine, you should download the RubyInstaller from the site https://rubyinstaller.org/ . 
This also will get the RubyGems along to this package, which will allow to install the web-framework Rails.

{{< figure src="/img/img24.png" title="RubyInstaller" >}}

After installation, check on the CMD if Ruby is installed by using the command : ruby -v

{{< figure src="/img/img1.png" title="Ruby installed on Windows" >}}


*Some Ruby Installer will include the MSYS2, which a Unix-like environment, a command-line interface for those who are used to Unix Shell Script commands. 
The installation of this component is optional.

<h3> <strong> Step 2 - Install Rails (Windows/Mac) </strong> </h3>

Go to the CMD(for Windows) or Terminal(for Mac) and use the command : gem install rails

{{< figure src="/img/img2.png" title="Rails installed on Windows">}}

{{< figure src="/img/img18.png" title="Rails installed on Mac" >}}

After installation, check on the CMD(for Windows) or Terminal(for Mac) if Rails is installed by using the command : rails -v

{{< figure src="/img/img4.png" title="Rails installed on Windows">}}

{{< figure src="/img/img19.png" title="Rails installed on Mac" >}}

*Puma WebServer is built-in with the installation of Rails.


<h3> <strong> Step 3 - Install MySQL and MySQL gem (Windows/Mac) </strong> </h3>


You will need to configure MySQL on your environment, if you to work with a database. Go to https://dev.mysql.com/downloads/mysql/ and configure MySQL server.

{{< figure src="/img/img5.png" title="MySQL website" >}}

After installation, go to the CMD(for Windows) or Terminal(for Mac) and use the command : gem install mysql2

{{< figure src="/img/img6.png" title="Gem MySQL installed" >}}

<h3> <strong> Step 4 - Choose a text editor (Windows/Mac) </strong> </h3>

You can use any text editor to code with Ruby. However, I suggest to use one colored text editor, in order to make easy to code and identify the elements of Ruby programming language.
Here a few suggestion of text editors:

Atom
https://atom.io/

Sublime
https://www.sublimetext.com/

Notepad++
https://notepad-plus-plus.org/

<h3> <strong> Step 5 - Create a new project (Windows/Mac) </strong> </h3>

On the CMD(for Windows) or Terminal(for Mac), choose the folder you want to create a project. After that, use the following command : rails new <project_name> Ex: rails new helloworld

Now you have a folder with your project created.

{{< figure src="/img/img7.png" title="Create Ruby Project" >}}


<h3> <strong> Step 6 - Create the database (Windows/Mac) </strong> </h3>

With the installation of MySQL, there is a command-line called "MySQL XX Command Line Client" that we can use to connect to the database server. Connect to MySQL and create the database 
by using the following command : 
CREATE DATABASE <database_name>; Ex.: CREATE DATABASE helloworld_database

Then, grant access to your rails application by using the following command :

GRANT ALL PRIVILEGES ON <project_name>.* TO 'rails_user'@'localhost' IDENTIFIED BY '<password>';

{{< figure src="/img/img9.png" title="Create DATABASE MySQL" >}}

Finally, enter on your text-editor and configure the file database.yml in the config folder. Include in the file the information of database, user and password passed to MySQL.

{{< figure src="/img/img11.png" title="Project Folder" >}}


{{< figure src="/img/img12.png" title="database.yml" >}}


To test if your project is connecting to the database go to the CMD(for Windows) or Terminal(for Mac), and use the following command : rails db:schema:dump.

This will create a new file called schema.rb in the db folder.

{{< figure src="/img/img13.png" title="Connect to database by your Rails Web Application" >}}

{{< figure src="/img/img14.png" title="schema.rb created" >}}

<h3> <strong> Step 7 - Launch the project </strong> </h3>

On the CMD(for Windows) or Terminal(for Mac), go to your project folder and use the command : rails server

{{< figure src="/img/img15.png" title="Launch Ruby on Rails Web Application on Windows" >}}

{{< figure src="/img/img21.png" title="Launch Ruby on Rails Web Application on Mac">}}

Go to the browser and check if the website is online. On my machine, the address is http://localhost:3000

{{< figure src="/img/img16.png" title="Ruby on Rails Website on Windows" >}}

{{< figure src="/img/img22.png" title="Ruby on Rails Website on Mac" >}}



<h2> <strong> Congratulations!!! You launched your first Ruby Application!!!  </strong> </h2>

References : 

https://prograils.com/posts/top-10-famous-sites-built-with-ruby-on-rails

https://www.netguru.co/blog/pros-cons-ruby-on-rails	

https://www.ruby-lang.org/en/about/

http://rubyonrails.org/

https://rubygems.org/

https://www.lynda.com/Ruby-Rails-tutorials/Installing-Running-Ruby-Rails-5-Windows/500550-2.html



