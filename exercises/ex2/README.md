# Exercise 2 - Create an API (Service)

After the creation of the persistence layer we will now make sure to expose the data via an API. Let's get started.

## Exercise 2.1 Create a service
You can now close the Date Model Editor if you like or you can switch directly back to the "Home" tab in the Application Studio.

You home tab displays the three entities in your model and you can easily navigate back to the Data Model Editor by clicking on of the Enities.

Anyhow, click the "+" sign in the "Service" box to create a new service. A services provides the API that your project will expose for the UX or other consumers like Workflow to be consumed. We will create the Apps (UX) in a later excercise.

The Serice Editor appears and asks you to create a service. Fill in the details as follow and confirm with a click on "Create", you can start by selecting the "Type" and the by changing the "Name":

![](/exercises/ex2/images/Service_01.png)

Repeat this step to create also services for Customer and Order, by going back to the "Home" tab and pressiong "+" on the "Service" tile. fter this tyour editor will look like this:

![](/exercises/ex2/images/Service_02.png)

Please note that the associations will be provided automatically, based on the definition in the data model.

As a final step for our service we add the "Draft Editing" mode in the "Property Sheet".  
First, click on the "HeroService" box, then click "Draft Editing" in the "Property Sheet" on the right hand side.  
You can double check how it should look like in the screenshot above. ("Draft editing" on the service enables a UX pattern where users can save erronous or incomplete data for themselves before activating the finished dta set for other users)

Close the Service Editor and navigate back to "Home" tab.

Note: If you accidently closed all the tabs you can find your "Home" tab by clicking on the "Project Explorer" icon on the left hand-side and click "Home" as depicted in this screenshot:  
![](/exercises/ex2/images/Service_03.png)  
You should have three entites in the Date Model and three services in the Service box.

Next task will be to add some sample data so that we can test run our service.

## Summary
You have now added a service to your project. Essentially, this service will expose your data model as an OData V4, RESTful API to your application.

Continue to - [Exercise 3](../ex3/README.md)
