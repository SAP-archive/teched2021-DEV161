# Exercise C - Create the Pages/UX
In this unit we will create the user experience for our app and will run a preview on your mobile device. Please make sure you have downloaded the AppGvyer preview app to your mobile device. There is no need top open it at this point in time.

## Excercise C.1 Create the Hero Catalog Screen

Navigate back to the "Empty page" main page view of AppGyver, by toggling back to "view" from "variables" in the upper right corner.

Cange the "Headline" to "Available Heroes" by selecting it and changing the property "Content" in the "PROPERTIES" tab on the right.

Now, select the "STYLE" tab, expand the "DIMENSION AND POSITIONING", and scroll down until you see the "Align self" area.

Select alignment center as depicted below:

![](/exercises/exC/images/UX_01.png)

On the "STYLE" tab, you can influence the visuals of your controls.

Now select the paragraph right below your headline and change the "Content" property to this text:
```
Browse our catalog of available heroes. You can book them for your birthday party or to join you to smash the evil villian.
```
![](/exercises/exC/images/UX_02.png)

Now we will add our first new control to the page.

From the palette on the left, choose the "List item" and drag it right below the paragraph.

Now, in the "PROPERTIES" tab on the right, click on the small box under "Repeat with". The following dialog will appear. Here you can select the value for the "Repeat with" property. It can come from various sources, but in our case we want to bind the property to our list of heroes we defined earlier. 

Select "Data and Variables"

![](/exercises/exC/images/UX_03.png)

The next screen let's us choose from various variables of different scopes an purposes. Select "Data variables" as we want to retrieve our list of heroes from the API. You will also notice that many options are disabled, because they are not available in the current context. This is one of many examples where AppGyver supports you in avoiding mistakes.

![](/exercises/exC/images/UX_04.png)

Since we only have one data variable, choose HeroCatalog1 and confirm by clicking "SAVE".

You have now established a data binding between your control "List item 1" with the data variable "HeroCatalog1". Going forward AppGyver will make sure that the list will always be kept in sync with your data.

Now we also need to tell the control (List item 1), what properties of the Heroes should be displayed.

Click on the "ABC" button below the "Primary label" to open another dialog.

This time, we choose "Data item in repeat".

Now select "current", then "PublicName". Also provide a preview value.

It should look like this:

![](/exercises/exC/images/UX_05.png)

Confirm with a click on "SAVE".

Now add a static text for the "Secondary label" as follows (You can just paste it into the field next to the "ABC" button)
```
Book now
```

Back on the UX canvas, click "SAVE" in the upper right hand corner to save all your changes into the project.

Now it's time to test if your appication works so far.

## Excercise C.2 Preview Your Application

On the top navigation bar, click on "LAUNCH".

Here you can control the preview, distribution and release management of your app. Today we will concentrate on the "PREVIEW" part.

As you can see, you can preview as webapp, mobile apps, macOS desktop app and even on Android TV.

Click on "Reveal QR code".

Now it's time to open the "SAP AppGyver Preview" app on your mobile device.

![](/exercises/exC/images/UX_06.jpeg)

And touch on "SCAN QR CODE" button.

After allowing the app to access your camera, you can can scan the previously revealed QR code.

You will be automatically logged into your account and will see a list of all your active projects in AppGyver.

Select the "HeroRent0XX" app by touching the "OPEN" button.

All your data entries should appear now. It should look like this:

![](/exercises/exC/images/UX_07.jpeg)

From now on you can leave this app open - all changes will appear here automatically, allowing you to quickly validate every change you make.

Our quick check has discovered that the title of the page shows "Empty page". So, let's fix this.

Back in AppGvyer, close the "LAUNCH" perspective by pressing the "x" in the upper right corner, you should now be back on the page view. Now select the PAGE LAYOUT in the lower-right component tree view and set the "Page name" property to "Catalog" and the "Short description" to 
```
Displays a list of available heroes
```

Confirm by clicking "SAVE" and save your project. After a few seconds your app on the mobile device is reloaded updated.

## Excercise C.3 Adding the Order Page

In order to add a new page, we click on the link labled "Catalog" in the upper left corner of AppGyver.
Here we see all our current pages and can add, or remove pages. Also we see here a "Global canvas". Here we could model non-UI related logic into the applicaton. 

Click on the "ADD NEW PAGE" plus sign on the left. A dialog appears and asks you for a new page name. Provide the name "New Booking".

Immediately, a new page will appear in the page canvas and we can start adding our UI controls.

Add the following controls to your page:
1. "Button" - label it "Select Date"
2. "Dropdown field"
3. "Input field"
4. "Row" - from the LAYOUT section
5. "Button" - into first column
6. "Button" - into second column.

It should look like this::

![](/exercises/exC/images/UX_08.png)


Save your changes.

## Excercise C.4 Adding variable to our page

Before we go ahead and make the page look better, we will create some variables and parameters.

Switch to the "VARIABLES" view (upper-right corner).

On the left,select "PAGE VARIABLES".

Click "ADD PAGE VARIABLE" plus sign to add avariable to the list.

Give your first variable the name "bookingDate" in the property editor on the right.

Select "Date/time text (ISO 8601)" as the "Variable value type".

Create two more page variables:

| Name          | Type          |
| ------------- |---------------| 
| duration      | text          |
| remark        | text          |


Save your changes. Is should look like this:

![](/exercises/exC/images/UX_08a.png)

Now we add a page parameter by selecting the "PAGE PARAMETER" on the left menu.

A page parameter ensures that this page will receive information from the previous page in the navigation. We want to pass the GUID and the PublicName of the selected hero from the Catalog page. 

Add the following page parameters:

| Name          | Type          |
| ------------- |---------------| 
| HeroGuid      | text          |
| HeroName      | text          |

Save the changes by clicking "SAVE" button.

![](/exercises/exC/images/UX_09.png)

Switch back to the page canvas by selecting "VIEW" in the upper right corner.

## Adding Formulas

We will now add some logic and behavior to our order page by using formulas.

Select the first paragraph, still labeled with "Lorem ipsum..." and click on the "ABC" button of the "Content" property on the right.

In the dialog poping up, select "Formula". You can use formulas almost everywhere in AppGyver. 

In the next dialog click on the "Lorem ipsum.." text under "Formula" to select open the Formula editor.

![](/exercises/exC/images/UX_10.png)

On the top you see your current formula to edit. Underneath to the left, is a list of all available functions and on the right you see a preview pane and an area where errors and hints will be displayed.

For this formula we want to display the incoming page parameter of the selected hero and add some additional text by concatinating some literal text.

Add the following formula into the formula field (replace the original content)

```
"Hero to book: " + params.HeroName
```

If you type this, you will see various hints on what you can potentially use in this editor.

Save your formula by clicking "SAVE", closing the dialog.
If you want to provide a better preview value, you can choose a preview value in for the page parameter.

Confirm the dialog with "SAVE" to apply your formula.

## Adding a UI Component from the Component Market

The list of components in the palette is not everything. For our mobile users to select a date and time for the booking we will add a DateTimePicker from the Component Market.

Open the logic editor on the bottom by clicking the dark grey area.

On the top-left, click on "COMPONENT MARKET" and search for "datetime" under "frontend logic" and select the "Pick datetime" box.

![](/exercises/exC/images/UX_11.png)

Click the "INSTALL" button to add this flow component to your project. AppGyver will now manage this dependency and notify you about updates that are being provided in the future.

Make sure you have selected the "Select Date" button in your page view and the "INSTALLED" tab in the logic canvas.

Now drag the "Pick datetime" flow function to the logic canvas.

Drag a line from the flow "EVENT Component tap" to the Dialog flow.


We have connected our app to our CAP API and tested it succesfully. We also checkk the data retrieval logic.

It should look like this:

![](/exercises/exC/images/UX_12.png)

By connecting the dots (literally) you implement the behavior of your app. Essentially, we just said that if "Select Date"-button has been tapped, open the Pick datetime dialog.

The dialog needs some mandatory inputs as you can see on the right hand side, in the PROPERTIES pane. Let's provide these values.

Click on the "ABC" button under "Minimum date", click "Formula" and select the "" formular to provide a new one:

```JAVASCRIPT
DATETIME(NOW())
```

Save the formula and provide the following formula for "Maximum date":

```JAVASCRIPT
ADD_DURATION(NOW(), 60, "days")
```
Save this formula as well. 

We just defined that we will not let users choose a value later than 60 days in the future.

Also provide the optional input for "Initial datetime" as

```JAVASCRIPT
NOW()
```
So that we have an initial value. 

The full definition should look like this:

![](/exercises/exC/images/UX_13.png)

Now we want to store the selected value in our page variable. 

Select the "CORE" tab in logic palette and drag the "Set page variable" to the logic canvas. Connect the "Pick datetime" and the "Set page variable" with a new line. Make sure you start the line from the upmost connector of "Pick datetiem".
Select the new node and click on the box below "Variable name" on the right to assign our page variable "bookingDate" to it.

Now click the "ABC" button under "Assigned value" to assign the value from the previous dialog to the bookingDate variable.

In the dialog click "Formulas" and add the following formula:

```JAVASCRIPT
outputs["Pick datetime"].pickedDatetime
```
Save your changes.

Validate your changes:

![](/exercises/exC/images/UX_14.png)

We ignore the other outputs of the "Pick datetime" dialog for the moment, but with the help of these you can react on dialog cancel or error.

## Finishing the other UX controls
Select the dropdown list in the UI canvas of the New Booking page.

Add "Duration" as a label using the "Label text" property.

Click the "Option list" property on the right. Use the dialog (use the "Add another value" link) to add three values and labels for each (like "1 day" and 1, "2 days" and 2, ...).). It looks like this:

![](/exercises/exC/images/UX_15.png)

Set the "Selected value" to our page variable "duration", by using the dialog. You open the dialog by clicking the box under "Selected value". This step binds the value of our drop down box to our page variable.

Save your changes.

Now, select the Input field under "Duration" and put "Remark" as the Label and set the "Value" property to the page variable "remark".

Save your changes.

Two buttons to go. Select the left button and label it "Cancel". Also change the style to a light grey by using the "Style"-property page. (Hint: Background color).

Now, while the cancel button is still selected, drag the logic flow "Naviagate back" from the palette to the logic canvas and connect it to the "Component tap" node.

Double check your result:

![](/exercises/exC/images/UX_16.png)

Save your changes.

Select the remaining button. Label it "Book Now" and choose a nice background style color (e.g. #79aec3).

Now we will add the booking logic. Once the user provided all the necessary values we want to send it to the backend API and store a new row in the database.

While the "Book Now" button is selected, drag the "Create record" flow from the palette to the canvas and connect it to the "Event Component tap" of our button.

Use the properties dialog under "Resource name" to select the "MyOrders" service as the target API to talk to.

Then click on the "Custom object". Here you can see all the expected input field of our API. Our task now is to map it to our variables.

![](/exercises/exC/images/UX_17.png)

For the ID, we will provide a formula as follows:

```JAVASCRIPT
GENERATE_UUID()
```
OrderFrom will be our bookingDate page variable. 

OrderTo is the a formula as follows:
```JAVASCRIPT
ADD_DURATION(pageVars.bookingDate, pageVars.duration, "hours")
```

Remark is just our page variable "remark".

And orderedHero_ID is the incoming pageParameter HeroGUID

Here you can compare your editings:

![](/exercises/exC/images/UX_18.png)

Save and close the dialog.

Save the changes on this page.

After creation of the record, we want to navigate the user back to the Catalog page, so drag the "Navigate back" node to the logic canvas and connect the first output node from "Create record" to our navigation.

In case there is an issue with the order, let's notify the user. Drag the "Alert" node to the logic canvas and connect the error output node from "Create record" to the dialog. 

Also provide an error message to the "Dialog title" property.
BONUS: Select the output of the previous node to see the actual error message.

The overall flow should look similar to this:

![](/exercises/exC/images/UX_19.png)

Save your changes on this page.

## Adding Navigation from Catalog to Booking Page

Close the "New Booking" page by clicking on the "New Booking" page in the toolbar on the left and open the Pages overview to and open the "Catalog" page.

Select List item 1 and make sure the logic canvas is open.

Drag the "Open page" node to the logic canas and connect it with the "Event List item tap".

Select the navigation node and select the page to open as "New Booking". Since this page has page parameters, they are listed here and can be populated.

Select the value help box under "HeroGuid" and select "Data item in repeat", then "current", then "ID". Save to close the dialog.

Repeat the step for "HeroName" and select "Data item in repeat", then "current", then "PublicName". Save to close the dialog.

![](/exercises/exC/images/UX_20.png)

Save the changes on the page.


## Validate Your Application 
On your mobile device, opene SAP AppGyver Preview, open the HeroRent0XX app and check all the functionality we implemented so far.


## Summary

This concludes this exercise.

