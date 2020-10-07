# Meadows Of Stockholm

Full Stack Frameworks with Django Milestone Project MS4

[Meadows of Sthlm](https://meadowsofsthlm.herokuapp.com/)

# About

## Project scope

This project is part of the 'Full Stack Frameworks with Django' module of the Code Institute Full Stack Software Development course.

To complete this module the task was to create an issue tracking application that allows users to submit their tickets.

The site is built with Django framework, deployed live on Heroku and uses AWS S3 to host media and static files. Locally, it uses the built-in Django Db.sqlite3 database, whereas when deployed live it uses Heroku's Postgres database. Their is full authentication functionality on-site using Django's Allauth: admin superusers can add and edit items in the Antiquities and Latest Options apps, whereas normal users can register and login, gaining access to antiquity descriptions and their order history in the Checkout and Profile apps.

# User Experience

I wanted the user experience to be as simple and clean as possible. No annoying popups, only clean product images.

## User Stories

### The Unauthenticated Site User

- As an Unauthenticated Site User, I can browse all products
- As an Unauthenticated Site User, I can browse all products and sort and filter by name, price, rating and category on the All products page.
- As an Unauthenticated Site User, I can select my chosen products and then go to the Cart Page to review my order.
- As an Unauthenticated Site User, I can navigate from the Cart Page to the Checkout Page to enter my billing details and finalise purchase without a profile

### The Authenticated Site User

- As an Authenticated Site User, I can Register to create a New Profile from the navbar.
- As an Authenticated Site User, I can Login to my previously created profile from the navbar and gain access to purchase history
- As an Authenticated Site User, I can Login and view my User Profile, along with my Order History, via the link in the navbar.

### The Site Administrator

- As a Site Administrator, I can create a Superuser Profile through Django.
- As a Site Administrator, I can access my Superuser Profile by typing the '/admin' url into the browser.
- As a Site Administrator, I can access all orders, emails, users and app fixtures by viewing the Django admin backend.

## Design

I used Adobe XD to create mockups for the site. I used Adobe Photoshop to edit image colors to fit the same color theme.

### Images

Images are taken from Pexels, Pinterest, Shein and Google images

### Fonts

I used Hoefler serif font for the logo and and Nobel for fine text.

### Icons

I used Friconix for cart and user icons and Font Awesome for all other icons.

### Wireframes

![Wireframe](https://res.cloudinary.com/www-madine-se/image/upload/v1602032395/Web_1920_2_h4llf1.png)

### Design Changes

Due to time constraint I had to drop a lot of the initally planned designs and features.

## Features

### Home App

This the is main template for the site, which contains the Head and Footer and Navbar elements for every other page, route or view.

- This Navbar is the fully responsive navigation element. It contains links to the following screens: Home, Latest Options, All Antiquities, Cart, links for Login, sign up. There is also a Cart Total icon, a Search icon. Navbar element collapses to a dropdown on smaller resolutions.

- The Footer is a basic element that contains a small Copyright text. The links in the navbar also appear here, and become a dropdown on smaller devices.

### Main Page

The games opening page, containing the main logo and some information about the site, along with the Landing Page Background which is an image of the Parthenon in Athens at night. There is also a CTA button asking the user to 'Donate Now'.

### Cart App

This page has two main sections: a Shopping Cart Detail section, with image, name, quantity and value of each item; a Cart Total section with a list number of items and the total price. Quantity can be changed for each item here, and the edit and delete options for supperusers appear again.

### Checkout App

where the user's order is detailed once more (but without the update, edit or delete options); Checkout Information section, where the user inputs their billing info and credit card details before checking out. The credit card section is linked to and enabled by Stripe. The form needs to be fully validated before submission. As with the Cart App, the two sections appear side by side on larger resolutions, and above one another on smaller resolutions.

### Profiles App

Once again this page has two main sections: Default Billing Information where the billing information the user has used for previous orders appears and can be updated; the Checkout information section, where each previous order appears with its order number, date, item name x quantity, and order total information visible. The user can click through via a link on the order number to the full details of the original order in the Order History view As with the last two apps above, the two sections appear side by side on larger resolutions, and above one another on smaller resolutions.

### Future Features

- Pagination
- Blog
- Featured products
- Social links
- Favorites app

## Technologies Used

All the technologies used to create this project are listed below:

- HTML
- CSS
- JavaScript
- Python3
- Git and Github
- Heroku
- AWS S3 and IAM
- Django
- Postgres
- VSCODE
- Bootstrap
- Adobe XD
- Adobe Photoshop
- TinyPNG

## Validators

- [Html](https://validator.w3.org/)
- [CSS](https://jigsaw.w3.org/css-validator)
- JavaScript - JSHINT extension on VSCODE
- Autopep8 on VSCODE

## Testing

Devices and platforms used for testing:

- Iphone X
  - Safari
  - Chrome
  - Brave
- Ipad Pro 12.9" 2018
  - Safari
  - Chrome
- MacBook Pro 13" MacOS Catalina
  - Safari
  - Chrome
  - Firefox
- MacBook Pro 13" Windows 10
  - Chrome
  - Firefox
  - Microsoft Edge
- OnePlus 5T
  - Firefox
  - Chrome

## Manual Testing

I tested the site in Developer Tools mainly in Chrome and Safari. Bugs and errors were tackled successfully in this way throughout the development process by using lots of print statements.

Tested all functionality by clicking on all elements and buttons:

- Any user can create their own account by using the registration form. User has to provide first and last name, username, email and password in order to register.
- Login form enables user to login to their account. Whenever user wants to log out they can click 'Sign out' located in the navbar menu. When user is not authenticated nobody else can access their account unless they know username and password of that user.
- User can add products with 'Add to cart'. User can then press "Checkout" button to fill out their data and finalise purchase.
- User is able to filter out products by type and status by using the filter feature implemented on the all products page.
- User is able to search throught the content of my application by using the search bar.
- User can access the edit profile form by clicking 'Edit Profile' in the navbar or on their profile page.
- If user forgets their password they can click 'Forgot your password' link available on the sign in page. Process is designed in a way to provide a clear instructions every step of the way.
- Users can view their purchase history in their profile if they have registered.

## Bugs

Most of the errors I encountered along the way were simply syntax mistakes.

I ran into a bug when connecting to Postgres that took a couple of days to find. I tried manually migrating it, but ran into more and more errors. Addind `release: python manage.py migrate` to procfile solved the issue.

Failed to load Friconix.js file on deployed app. Fixed the issue with CDN

# Deployment

## Run Locally

To run project locally on Mac Os:
Clone repo `https://github.com/sabinemm/meadows_of_sthlm.git`

Make sure you have python and pip installed/upgraded and run each of these commands:

```
python3 -m pip install --upgrade pip

pip3 install virtualenv

virtualenv env

source env/bin/activate

pip3 install -r requirements.txt

python3 manage.py runserver
```

You will need to set environment variables both locally and on Heroku Config Vars for `SECRET_KEY` etc that are found in settings.py.

### Heroku

To push the code to a Heroku and deploy it dynamically, follow the steps below.

Procfile is a Heroku specific type of file that tells Heroku how to run our project;

For the Procfile run

```
echo web: gunicorn meadowsofsthlm.wsgi:application > Procfile
```

command in the terminal;

Create an App on Heroku. Log in to your previous Heroku account or set up a new one, select the New button on the top right of the screen, then select Create New App.

Next, login to your Heroku account from your CLI using:

```
heroku login
```

A browser window should open up where you can click to login to your account through your local IDE. If this does not open, select the link on the CLI with ctrl + c and open it manually.

Link your existing Git repository to Heroku by adding Heroku as a remote repository:

```
heroku git:remote -a <project-name>
```

From now on you can push your code from the CLI with:

```
git push heroku master
```

Set the necessary Environment Variables. Select the Settings tab, and then select the Config Vars button. Enter the KEY - VALUE pairs for your config variables here (e.g. SECRET_KEY, IP, PORT etc.)

In order to migrate all the models into Heroku PostgreSQL I run

```
heroku python3 manage.py makemigrations
```

and

```
heroku python3 manage.py migrate
```

To create a new superuser in the new PostgreSQL database I ran createsuperuser command;

Finally, select the Open App button the top right of the screen to see your deployed application.

### AWS

To use AWS S3 to store staticfiles I set DISABLE_COLLECTSTATIC=1 by running the following command:

```
heroku config:set DISABLE_COLLECTSTATIC=1
```

## Credits

### Code Used

Readme content inspiration taken from several CI student projects. Followed CI tutorials.

### Images Used

- Pexels
- Shein
- Google Image Search
- [Pinterest](https://www.pinterest.com/pin/434034482838015620/?nic_v2=1a5x4ftaT)

### Acknowledgements

Thanks to my mentor Maranatha Ilesanmi for supporting me through this project.

### Disclaimer

This is for educational purpose only. If there is any issue with images, please email me at sabine.mica@gmail.com for them to be promptly removed.
