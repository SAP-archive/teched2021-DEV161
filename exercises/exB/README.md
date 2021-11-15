# Exercise B - Create a Data Source
In this exercise we will connect our AppGyver app to the CAP-based service we depolyed in Part 1.

## Excercise B.1 Add a Data Resource to our Application

In AppGyver, select the "DATA" tab in the top navigation bar.

Click on the "ADD DATA RESOURCE" sign on the right-hand side.

In the dialog select "OData integration". CAP by default exposes OData V4 compliant services and AppGyver by default consumes OData V4 compliant services - a perfect fit.

Copy the URL of our CAP Service and append "/consumer" (The URL you should have noted down [here](../exPrep#find-our-odata-service))

here's an example (please replace and insert your user number)
```URL
https://techedlcap-lcapteched2021-dev-techedlcap001-srv.cfapps.eu10.hana.ondemand.com/consumer
```
and click the "Verify URL" button.

On the left, you should now see HEROCATALOG and MYORDERS. Active that toggle next to it for both services. It should now look like this:

![](/exercises/exB/images/DATA_01.png)

Once this is done, click on "SAVE DATA RESOURCES" button to confirm the dialog.
In a real world scenario with actual authentication, we would need to add the autentication type, but we keep it simple for learning purposes here.

The DATA Resources should now show two entries: HeroCatalog and MyOrders.

AppGyver needs constant, manual SAVE steps. So click on "SAVE" on the right side to perform a save action. In addition, AppGyver takes care of maintaining a history, so you can rollback you changes anytime.

## Test run 

AppGyver already retrieved the OData metadata in order to populate all the needed information to communciate with the service. Anyhow, let's double check if we can really retrieve the correct data.

Click on The "HeroCatalog" line item.

In the dialog which appears, click on the "List" menu item on the left.

Now, select the "Test" tab.

Scroll down to the very bottom of the dialog and click the "RUN TEST" button.

You should see your data in the black area of the screen as expected:

![](/exercises/exB/images/DATA_02.png)

Close this dialog with the "X" button in the upper-right corner.

Navigate back to the Page view by clicking the "Empty page" link in the upper-left corner and then clicking on the actual empty page or pressing the "X" button in the upper-right corner.

We will now add a "Data variable" to make sure we have an in-memory, runtime represenation of the data we want to retrieve from our back-end.

Switch to the "Variabes" view, by toggling the button to the right. (you find this switch in the upper right corner of the screen, a toggle between "view" and "variables")

In the menu on the left, click "DATA VARIABLES".

Now click "ADD DATA VARIABLES" "+"sign on the right.

From the drop-down list, select "HeroCatalog". It should now look like this:

![](/exercises/exB/images/DATA_03.png)

Please note, that on the right hand side, this variable represents a "Collection of data record" and fetches all data. This is where you could now influence how your app will retrieve your data by adding filter conditions, influence ordering and so on. Also authentication is managed here.

But there is one more thing about the data variables which is important.

Click on the "Show logic for Empty Page" in the grey bar on the bottom of the screen:

![](/exercises/exB/images/DATA_04.png)

Here you see how and when the data is actually been retrieved and what happen to it. Let's have a closer look:

ON: Page mounted //This is when it appears on the device (start/focus/awake...)

Step 1: Get record collection //This is the actual HTTP request to the back-end service

Step 2. Set data variable //Stores the HTTP repsonse into variale HeroCatalog1

Step 2.1 Delay //Wait 5000 ms

Repeat with Step 1.

You see that here was a loop implemented where each second the data will be reloaded.

This is very convenient for testing purposes, but it will impact your back-end performance in production negatively. For now we will leave it as is. But if you want, you can select the "Delay" node and just delete it.

Click "SAVE" to persist your changes.

This concludes this exercise.

## Summary
We have connected our app to our CAP API and tested it succesfully. We also checkk the data retrieval logic.

Continue to - [Exercise C](../exC/README.md)
