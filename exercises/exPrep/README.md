# Getting Started - Perparation Part 2

The first deployment can take some time ( a couple of minutes), but subsequent deployments usually work much faster. After the deployement has finished sucessfully, we need to verify it and collect some information as well as we need to make sure our users can access the deployed apps. 
Therefore, we will perform some administrative tasks in this chapter.


## Verify Deployment Amd Assign Authorizations

Open a new browser tab andlogin to the following page with your provided session credentials:

```URL
https://cockpit.eu10.hana.ondemand.com/
```
You can simply click this [link](https://cockpit.eu10.hana.ondemand.com/).

This is the starting point for the admin cockpit of SAP BTP.

![](/exercises/exPrep/images/Prep_01.png)

As your user is a subaccount administrator only, you have no further options on this level. So the next step is to click on the "TechEdLCAP-Dev" subaccount box to navigate to the subaccount.

As you your user for this workshop is subaccount administrator you can see all the services and resources which are currently running in here. This is plenty since all the users of workshop use the same subaccount.

![](/exercises/exPrep/images/Prep_02.png)

In the left hand menu, click  on the menu item "Users". Find your user in the list and select it. You can use the "Search" functionality on the top to do so. Then, select the row with your user. A slide-in on the right hand-side will show all the Role Collections which have been assigned to your user.

The applications we developed in Part 1 are automatically protected by some access controls. So at the moment nobody, not even our subaccount administrator can access them. Let's change that.

Click on "Assign Role Collection" right besides the search bar on the right to add a new role collection:

![](/exercises/exPrep/images/Prep_03.png)

Now, use the search field to find your username, e.g. TechEdLCAP0XX, where XX is your user number. You'll find a Role Collection which follows the convention {USERNAME}Manager-dev. Select it and click "Assign Role Collection". 

![](/exercises/exPrep/images/Prep_04.png)

The Role and Role Collection have been defined by yourself (without your knowledge though) by using the Low-Code Perspective. You can change it any time later on, but we will not cover this in this session. The assigned Role Collection allows your user to access the deployed services. 

Next we will test our deployed apps.

## Test your apps

In the left-hand menu click on "HTML5 Application" to see a list of deployed web-apps in this subaccount.

Again, type your username in the searchbar and perform a search. For subaccounts with much traffic it is most convenitent to use the search, the lists can grow too quickly. 

![](/exercises/exPrep/images/Prep_05.png)

You see three apps being deployed:
1. HeroManagement - This is the Fiori Elements app for our backoffice to manage the heroes we can rent out.
2. OrderInsights - This is the app, which let's mangage the orders.
3. Launchpad - Where does this come from? We did not create a Launchpad app. Actually, this one was created to "embrace" all the apps of our project and give them a bit of a context. In a real-world scenario you would probably decide to not use it and deploy the Hero and Order app to a centralized Launchpad. But her it comes in handy.

Click on the Launchpad app. A new browse window will pop up. A launchpad with two tiles - our two apps.

![](/exercises/exPrep/images/Prep_06.png)

The list will appear empty, and in order to see your data, click on "Go". Actually, you can also make your app to pre-load all the data once the user loads the page, but we did not decide to do so.

Click on "Go" to see the sample data that we initially included during our development.

![](/exercises/exPrep/images/Prep_06.png)

You can play around with the app, add new heroes to your database by clicking the "Create" button, or you delete an item (only the new ones - the others are already booked), search and apply filters. You can even re-arrange the table columns. Remember, we did not write a single line of code in order to allow this.

If you want you can also check out the other "OrderInsights" app.

## Find our OData service

Once you are done trying out your services, close the browser tab and click on "Overview" in the SAP BTP Cockpit to navigate to the subaccount overview.

On the right hand you find a list of "Spaces", as we only have one - the "dev" space, click on the "dev-space row to navigate to our dev space.

Use the searchbar on your right and search/filter for your user name. You will find a {USERNAME}-srv application, which should be in the state "Started".

![](/exercises/exPrep/images/Prep_08.png)

Click on that service name and a detailed desciption page for this will open up.
What you see here is actually your deployed CAP service. 

![](/exercises/exPrep/images/Prep_09.png)

Here you can manually start, stop or delete your service and add more service instances to scale your app. Anyhow, we don't need to do that at the moment, but:

Copy the Application Routs to your notes/clipboard as we need it in the next exercise.

Once you have noted down the URL, click it to open our service:

![](/exercises/exPrep/images/Prep_10.png)

This should be familiar to you - we have seen this using our preview feature in the AppStudio. Please note that there are no Web Applications right now as they have been deployed to the HTML5 repository separately.

You can click on any service to test it out if you like. Please note that this time, the data you see is actually stored in the SAP HANA database running in the context of our subaccount. So all data changes will be persisted.

This conludes the validation and preparation phase.

## Summary
We assured that all necessay access rules are in place, our use can access the deployed app and we know where our service API is located.

Continue to - [Exercise A](../exA/README.md)
