# Exercise 4 - Add Your First App

In this step we will create a back-office application which allows our back-office employees to mangage the available heros, check the customer list and also see the orders.

## Excercise 4.1 Hero Management
First we build an Fiori Elements based application that let us create, update and delete our heroes in the database. You don't need any preexisting knowledge about Fiori Elements, and even if you have never heard about it you will be able to use it using the Low-Code development perspective here in the SAP Business Application Studio.

Back on the "Home" page, click the "+" sign in the "User Interface" box. A dialog will appear asking your for an Application Name and Description and Data source. Please make sure you provide the following values:

![](/exercises/ex4/images/App_01.png)

Make sure you select the correct Data source as displayed above.

Click "Next".

In the next dialog option you can choose between a "Template-Based, Responsive Application" which is tailored for use on a desktop browser, or you can choose "Mobile-Centric, Freestyle Application". The former maps the the Fiori Elements technology we use here, the later to Mobile Development Kit.

![](/exercises/ex4/images/App_02.png)

Choose the "Template-Base, Responsive Application" and click "Next".

Now that we have decided for the template-based app, we can choose between two different types of floorplan layouts. 

![](/exercises/ex4/images/App_03.png)

We choose "List Report Object Page", to display a list of our heros and click "Next".

In the next step we will select our Hero entity as the "Main entity" and let all the table columns be populated automatically. The Naviation entity should be "None":

![](/exercises/ex4/images/App_04.png)

Click "Finish". This will start the generation of a new "User Interface" for your app in your project. After a few seconds it is listed in the "User Interface" box.

If the User Interface editor does not open automatically, you can click on the user interace in the "User Interface" box.

Check out your new app in the preview window browser tab. If you accidently closed it, you can either CMD-click or CTRL-click on the green link on the bottom of your editor (http://localhost:4004)

![](/exercises/ex4/images/App_05.png)

You will notice that under "Web Applications" on the top you now see a new link, which ends on .../index.html. Click it.

You will see a preview Launchpad with one tile, representing our freshly created application. Congratulations!

![](/exercises/ex4/images/App_06.png)


But there is more! Click on the tile to open the app.

![](/exercises/ex4/images/App_07.png)

This is the List view, which is tied to the Hero entity. Click on the "Go" button on the right to list all your heros which are currently in your database.

Now you can see batman and Spiderman listed here. Also notice that there are several other options already here on the screen: You can create a new hero with the "Create" button. Try it out.

If you select one line item, with the checkbox in front, you can also delete the entry. Try to delete your freshly created item. Note that you can not delete the existing items we put into the sample data, since there are referential contrains in place. 

There are several more options on the screen. You can influence the displyed columns, you can drag and drop the columns to re-arrange them, you can even export the list or select the filters to incluence which data is displayed in the table.

Actually, we know have a complete CRUD-enabled application running, without writing a single line of code.

## Excercise 4.2 Order Insights

We also want to see the orders our customer have placed into the system. Go back to the "Home" screen and add another User Interface to the app by clicking the "+" sign in the "User Interface" box.

Provide the following details:

![](/exercises/ex4/images/App_08.png)

and click "Next".

Again, choose the "Template-Based, Responsive Application" option and click "Next".

Also choose the "List Report Object Page" and click "Next".

This time we choose the "Order Service" before we click "Finish":

![](/exercises/ex4/images/App_09.png)

Now let's check the app in the preview mode. You should now be able to find your preview alone.

The app should look like this:

![](/exercises/ex4/images/App_10.png)

We can now see the two orders nicely in our preview. Obviously, this app can be improved, but for now we just wanted to demonstate how to add multiple user iterfaces or apps to the project.

## Summary
This conclued this exercise and we have a complete application to allow our backoffice to work with the data. 

Continue to - [Exercise 5](../ex5/README.md)
