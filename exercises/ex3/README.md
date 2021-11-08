# Exercise 3.1 - Add some sample data

We will now populate our database with some sample data so that we can test our service.  
On the "Home" screen, click the "+" sign in the "Sample Data" box. A dialog will appear where you choose "Create" and "Customer".
A simple text editor will appear and you can overwrite its content with the following sample data:

## Customer
```
ID;EMAIL;FIRSTNAME;LASTNAME
8c1c3de7-547e-42e4-a62a-23b7646d7fc2;user@test.com;CustomerFirstName;CustomerLastName
```
If you want you can replace "CustomerFirstName" and "CustomerLastName" with better values.

Close the file and repeat the previous step for "Hero" - don't forget to choose "Create" in order to create a new file.

## Hero
```
ID;EMAIL;FIRSTNAME;LASTNAME;PUBLICNAME
ecfacc7f-2f5a-43c3-b031-9590305728d6;p_parker@test.com;Peter;Parker;Spiderman
81bed4a7-1539-40bc-8661-6c7279a30edb;the_real_batman@test.com;Bruce;Wayne;Batman
```  
Close the file.  

Finally, we also do the same for "Order". It's a bit hard to see, but the sample data is actually related to each other, since the GUIDs being used indicate that our one and only customer so far has placed two orders, each for one hero - for the same time. Apparently, this customer needs two super heros. 

## Order
```
ID;ORDERFROM;ORDERTO;REMARK;BYCUSTOMER_ID;ORDEREDHERO_ID
ID;ORDERFROM;ORDERTO;REMARK;BYCUSTOMER_ID;ORDEREDHERO_ID
d8ad9d86-a791-443e-8ac1-3c142170658f;2021-11-18T15:00:00.000Z;2021-11-18T19:00:00.000Z;Please bring latest costume;8c1c3de7-547e-42e4-a62a-23b7646d7fc2;ecfacc7f-2f5a-43c3-b031-9590305728d6
c6d0e969-d7f1-4e00-b0a3-f61e8a40a388;2021-11-18T15:00:00.000Z;2021-11-18T19:00:00.000Z;No weapons please;8c1c3de7-547e-42e4-a62a-23b7646d7fc2;81bed4a7-1539-40bc-8661-6c7279a30edb
```
Now all sample data has been provided and we will test drive our service now for the first time


## Exercise 3.2 - Run your app in preview mode

On the "Home" screen you find a "Preview" button in the upper right corner. Confidently, click it.

After a couple of seconds, you should see a toast alert in the lower right hand corner, which indicates that your app is now running in a new window.  
It can be that your browser will not open another tab, so please allow *.ondemand.com to open new tabs.
Alternatively, you can CMD-click or CTRL-click on the green link in the Task: Preview window on the bottom.

Switch to the new browser tab to see your current app in preview mode.

![](/exercises/ex3/images/Sample_02.png)  

From here you can navigate to the various deployment artifacts of your project. You can nav to the, currently empty, launchpad, to the $metadata resource of your API and do the three services we created and populated already with sample data.

Click on the "HeroService" link to open the API which provides the list of heroes in your database.

Please note that this services is run from an in-memory database, so any modification to the data will not persist.

We will later come back to this page once we add our user experience a.k.a apps.

Please leave this browser tab open. Whenever we change some of the data model, services, sample data or UX this tab will automatically refresh so we can immediately come back to see the impact of our changes.

## Summary
We have seen our service for the first time in action after we have added some sample data. Next we will add some apps.

Continue to - [Exercise 4](../ex4/README.md)
