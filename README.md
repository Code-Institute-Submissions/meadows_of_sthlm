# Meadows Of Stockholm

Full Stack Frameworks with Django Milestone Project MS4

[Meadows of Sthlm](https://meadowsofsthlm.herokuapp.com/)

# About

## Project scope

This project is part of the 'Full Stack Frameworks with Django' module of the Code Institute Full Stack Software Development course.

To complete this module the task was to create an issue tracking application that allows users to submit their tickets.

The site is built with Django framework, deployed live on Heroku and uses AWS S3 to host media and static files. Locally, it uses the built-in Django Db.sqlite3 database, whereas when deployed live it uses Heroku's Postgres database. Their is full authentication functionality on-site using Django's Allauth: admin superusers can add and edit items in the Antiquities and Latest Options apps, whereas normal users can register and login, gaining access to antiquity descriptions and their order history in the Checkout and Profile apps.

# Table of contents

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

### Design Changes

Due to time constraint I had to drop a lot of initally planned designs and features.

Features

Existing Features

Future Features

Technologies Used

Testing

Validation

Bugs
Deployment

Local
Remote
Heroku
AWS
Credits

Code Used
Images Used
Acknowledgements

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
