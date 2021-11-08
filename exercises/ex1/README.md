# Exercise 1 - Create a back-end with the SAP Business Application Studio

In this exercise, we will use the new low-code perspective in the SAP Business Application Studio to create a service, that persists our business data and exposes the data as an OData service for our consuming applications later on.
We will also test the service and see whether it runs or not.

## Exercise 1.1 Launch Low-Code Perspective

Open your browser an launch the followin URL:
```URL
https://lcapteched2021-applicationdevelopment.lcnc.cfapps.eu10.hana.ondemand.com/
````
You should see the central entry for low-code / no-code development on SAP BTP.
![](/exercises/ex1/images/lobby_01.png)

Click on the "Create" button and select "Business Application". A dialog appears where you can enter the following name for your project. As we plan to deploy our project it is important to stick to the naming convention here.  

**DO NOT USE YOUR OWN PROJECT NAME**  

Name your project  
```
TechEdLCAP0XX
```
Where XX is your user number. You can provide any descriptive text if you want.  
Confirm with a click on "Create".

After the SAP Business Application Studio has created your environment you should see a screen like this:
![](/exercises/ex1/images/LCAP_01.png)
Here we can build our project and use SAP-minded technologies such as CAP (Cloud Application Programming Model), Fiori Elements, MDK Mobile Development Kit and Workflow for our projects without thinking about how to structure our project and concentrate on the tasks to solve rather than spending time to think about project setup.

In the next step we will create a datamodel.

## Exercise 1.2 Create a Data Model

We will first create our persistence by adding a model to our project. Click on "+" sign in the Data Model box to open up the graphical editor for our data model.

Use the dialog to create our first entity as follows:
![](/exercises/ex1/images/LCAP_02.png)
Our first entity will have five properties to store a list of our heroes we want to rent out to our customers.
Please also not that we use all String datatypes except for the key, which is a generated UUID.

Confirm your model by clicking "Create".

We will now add another entity by pressing the "+" sign in the toolbar on top of the editor and select **Add Entity**.

![](/exercises/ex1/images/LCAP_03.png)

Now repeat the steps to create two more entities: Customer and Order.
We keep them simple as we do not want to emphasis on the E/R modelling capabilites in particular, but want to give you some insights about the productivity gains of the tool in general. The entity model should now look like this:

![](/exercises/ex1/images/LCAP_04.png)

We will now create an association between the entities to indicate who (Customer) orders (Order) whom (Hero).  
Click on Customer entity and click "Add Relationship".
Add the association as follows:
![](/exercises/ex1/images/LCAP_06.png)

and confirm by clicking "Create".  
Now click "Hero" entity and click "Add Relationship" again to create the following association:  

![](/exercises/ex1/images/LCAP_07.png)

Our data model is now complete an should look like this:

![](/exercises/ex1/images/LCAP_08.png)

## Summary

You've now create a data model including persistence in CAP (Cloud Application Programming model) that can be later used to be deployed to the SAP HANA database we will use. Note that you have not seen any CAP related commands or syntax.

Continue to - [Exercise 2](../ex2/README.md)

