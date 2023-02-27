[Link to deployed site](https://sdproject4.herokuapp.com/)

**Project Overview - What are we aiming for?**

A priority tracking app, allowing the user to specify their top 3 priorities, and then track their time on tasks. This will allow the user to see how much of their time is spent on priority and how much is spent off priority.

[![Wireframe Overview](/assets/images/mainpagewireframe.jpg)

**Are you tired of your old snow stuff?, do you need new?**

It is easy to be busy, and still feel as if you don't get anything done. This often happens when you don't know where your time goes. What are you really busy with? With this Priority Tracking App you'll see clearly how much of your time is spent on what is really important, and what is wasted away.

---
## Table of Contents
1. [**Why This Project**](#why-this-project) 
2. [**UX**](#ux)
    - [**User Stories**](#user-stories)
    - [**Wireframes**](#wireframes)
3. [**Features**](#features)
    - [**Existing Features**](#existing-features)
    - [**Features Left to Implement**](#features-left-to-implement)
4. [**Technologies Used**](#technologies-used)
    - [**Version Control**](#version-control)
    - [**Hosting**](#hosting)
5. [**Testing**](#testing)
    - [**Code Validation**](#code-validation)
    - [**Automated Testing**](#automated-testing)
    - [**Manual User Testing**](#manual-user-testing)
    - [**Interesting Bugs Or Problems**](#interesting-bugs-or-problems)
6. [**Deployment**](#deployment)
    - [**Local Deployment**](#local-deployment)
    - [**Remote Deployment**](#remote-deployment)
7. [**Credits**](#credits)
    - [**Content**](#content)
    - [**Acknowledgements**](#acknowledgements)
---
### Why This Project?
This project was initially created for people who has a pasion for snow sports. It is used to buy and sell snow products and have a conversation between users.

For the front-end I used HTML, CSS/tailwind. For the back-end I used Python, Django, SQLite3 and PostgreSQL.

## UX
This is simple POW Stop, focussed on selling and buying products, diferent categories and conversations.

Users can register/login and create their own Categories, post items, in a simple uncluttered interface.

### User Stories
"**_As a user, I would like to_** _____"
- register for a new account
- log into my existing account
- create my own categories
- list my own products
- list my products within categories
- see the price of each product listed
- see what products are related
- edit price and description of each product
- have a conversation with the owner
- undo a completed post
- delete products not required

"**_As a product owner, I would like to_** _____"
- assist users with resetting their passwords, in an automated fashion
- have full test coverage for Models, Views and Forms

### Wireframes
I used Balsamiq to create the wireframes and mock-up of the app. The links to the files are below:
- [Signup](/assets/images/signupform.jpg)
- [Login](/assets/images/loginform.jpg)
- [Main Page](/assets/images/mainpagewireframe.jpg)
- [New Item form](/assets/images/newitemform.jpg)
- [Dashboard](/assets/images/dashboard.jpg)
- [Browse](/assets/images/browse.jpg)
- [Inbox](/assets/images/inbox.jpg)

##### [back to top](#table-of-contents)
---

## Features
### Existing Features

#### Actions - serves as the main page for using the app
- **Navigation** - Simple navigation to access the New item, Browse, Inbox, Dashboard, Log in, Sign up. This is visible on all pages in the app.
- **Things I need to do** - This lists the existing products being worked on and the ability to add new products. For each product there is an option to Edit, and Delete. Also a option for contact seller.
- **Things I've done** - My items/Browse allows the user to undo and edit.

#### Categories - management of all Categories
- **Add a Category** - Allows the user to add a work Category, which is then used to categorise each product.
- **Edit a Category** - Allows the user to amend an existing Category.
- **Delete a Category** - Allows the user to delete an existing Category.

#### New Item - management of all New Item
- **Add a Item** - Allows the user to add Items, which can be nested under Categories, and used to link products.
- **Edit a Item** - Allows the user to edit an existing Item/Price/description.
- **Delete a Item** - Allows users to delete existing Item/Categories. Only owner of each item can delete.

#### Error Pages
-  Included are custom error handlers for 400, 403, 404 and 500 errors, with the option to navigate back to the desired section of the app. 


##### [back to top](#table-of-contents)
---
## Technologies Used
- [**HTML**]
    - The project uses **HTML** to create the pages and content of the app.

- [**CSS**]
    - The project uses **CSS** to apply the custom styles to the app.

- [**Bootstrap**]
    - The project uses the **Bootstrap** framework for styling.

-[**Tailwind css**]
    -The project uses **Tailwind Css** framework for styling and layout.

- [**Python**]
    - The project uses **Python** as the back-end programming language applied using the Django Framework.

- [**Django**]
    - **Django** was used for all aspects of creating the app. 

- [**SQLite**]
    - The project uses **SQLite** as the Database when running the project locally.

- [**ElephantSQL**]
    - The project uses Heroku's **ElephantSQL** relational database for the deployed version of the app.

- [**GitPod**]
    - I've used **GitPod** as the development environment when writing the code for the app.

### Version Control
- [**Git**]
    - **Git** is used as a version control system throughout the building of this app.

- [**GitHub**]
    - I use **GitHub** as a remote repository linked to Heroku when committing and pushing updates and changes.

### Hosting
- [**Heroku**]
    - The deployed vertion of the app is hosted on **Heroku**.

##### [back to top](#table-of-contents)
---

## Testing

### Code Validation
- [W3C HTML Validator tool](https://validator.w3.org/#validate_by_input) was used to validate all HTML code.
    - As W3C doesn't validate the Django Template HTML correctly, the validator remains showing some errors, but these are specific to the W3C compatibility with Django Templates. All standard HTML validates successfully.
- [Pep8 Online tool](http://pep8online.com/) was used to validate my Python syntax.

### Automated Testing
The [Coverage](https://pypi.org/project/coverage/) library was used throughout testing to help keep track of how much of my code was covered by the tests. The tests provide an overall coverage of 78% when including all files including files generated by Django.

You can generate a coverage report by installing the package using `pip3 install coverage`
- Run `coverage run manage.py test`
- Then `coverage html` to generate the report
- The report can be viewed in a browser by opening the `index.html` file from inside the `htmlcov` folder.

### Interesting Bugs Or Problems
- **When the web app was deployed to heroku i had a problem on the terminal, and it was fixed with heroku stack:set**

##### [back to top](#table-of-contents)
---

## Deployment
Using GitHub for version control and Heroku as the host for the deployed version of the site, I deployed to Heroku following these steps:

1. Create an app in Heroku using a unique name.

2. Under the **Resources** tab in Heroku, search for **Heroku Postgres** in the 'Add-Ons' section.

3. Selected the **Heroku Mini** level.

4. Updated the `env.py` file within my local workspace with the `DATABASE_URL` details, and the `settings.py` to connect to the database using the `dj_database_url` package.

5. Ran the `python manage.py makemigrations`, `python manage.py migrate`, `python manage.py createsuperuser` commands to migrate the models into Heroku Postgres and create a new super user in the new ElephantSQL database.

6. Went to the **Settings** tab in Heroku and clicked on the **Reveal Config Vars** button.


KEY | VALUE
--- | -----
DATABASE_URL | link to db |
HEROKU_POSTGRESQL_NAVY_URL | postgres API Key |

8. On the **Deploy** tab in Heroku, connect the Heroku App to the GitHub repository and select **Enable Automatic Deployment** as the deployment method.

9. Ensure `settings.py` references the correct Environment Variables for the Database Connections.


10. Update the `settings.py` file with the relevant configuration for static and media file storage.


11. Created a requirements.txt file using the following command in the terminal window:
    ```pip3 freeze --local > requirements.txt```

12. Create a Procfile using the following command in the terminal window:
    ```echo web: gunicorn puddle.wsgi:application > Procfile```

13. Ensure that the Heroku App has an associated Dyno for running the App

14. Run the `git add .`, `git commit -m "<commit-message>"` and `git push` commands to push all changes to my GitHub repository.

The app should be successfully deployed to Heroku.

### Repository Link

Visit the project's GitHub repository:

[GitHub Repository](https://github.com/FullStackSD/SDProject4)

### Running Code Locally

To run the code locally, you can follow these steps:

1. Go to my [GitHub repository](https://github.com/FullStackSD/SDProject4)

2. Select Clone from the 'Code' dropdown.

3. Copy the clone URL for the repository under the HTTPs tab.

4. Open 'Git Bash' in your local IDE.

5. Select the directory you want to use for the clone.

6. Use `git clone`, and paste the URL from step 3 above. 
    
    ```git clone https://github.com/USERNAME/REPOSITORY```

7. Press `Enter` to complete the clone process.

9. Install `requirements.txt` using the following command in your Terminal:

    ```pip3 install -r requirements.txt```

10. Run the following command in your Terminal:

    ```python manage.py runserver```

11. Click the `http://` link  or the `Open In Browser` button from the pop-up,to load the project.

12. Migrate the database models and create a super user:

    `python manage.py makemigrations`
    `python manage.py migrate`
    `python manage.py createsuperuser`


This will migrate the models and create your SuperUser account. You should now be able to run the site locally.

 To deploy the site remotely, follow the instructions in the [Deployment](#Deployment) section.

 ##### [back to top](#table-of-contents)
---

## Credits
#### Helpful Resources
-Thanks to the online tutors for all the help.
I also found a lot of examples and suggested solution to questions on Stack Overflow for specific issues I got stuck on.
- [Stack Overflow ](https://stackoverflow.com/)


#### Acknowledgements
- Thanks to the CI Slack community for help with the odd question.

##### [back to top](#table-of-contents)
---