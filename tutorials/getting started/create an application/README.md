# Honeycomb for Beginners: Getting Started

### Tutorials

* [Part 1: Creating your first Honeycomb Web Application](https://github.com/Schalltech/honeycomb-tutorials/tree/master/tutorials/getting%20started/create%20an%20application#part-1-how-to-create-your-first-honeycomb-web-application)

## Part 1: How to create your first Honeycomb web application

<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-11.png">

In the following tutorial you'll learn:

* how to create a basic Honeycomb Web Application
* how to add a page to your Honeycomb Web Application
* how to add a micro app to a pages layout
* how to style a micro apps container
* how to access your Honeycomb Web Application on the cloud

Micro apps you will use in this tutorial

Name | Description 
:---- | :-----
ma-label | The label micro app represents a caption for an item in a user interface.

### Create the Hello World Application
Creating applications with micro apps is fast and easy when using Honeycomb Studio. 

#### Step 1: Login
To get started, log in to your Honeycomb Studio account. 

<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-0.png">

#### Step 2: Create the application
Select the Applications tab on your account page and click the New button.

<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-1.png">

#### Step 3: Give your Honeycomb Application a name and description
Clicking the new button in the previous step will open the application editor so you can give your application a name and description. Enter "Hello World" as the applications name and "My first honeycomb application!" for the description. After entering the information, click the create button.

<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-2.png">

#### Step 4: Add a page to your Honeycomb Application
After clicking the create button in the previous step, your new application is displayed within the studio admin screen. From here we will need to add our first page to the application. Select the Pages tab and click the create button.


<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-3.png">

#### Step 5: Name your new page and give it a description
In this step, enter Home for the pages name and "Main landing page of the application." for the description. Click the create button after entering the information.

<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-4.png">

#### Step 6: Add a micro app to the page layout
The new page is now displayed in the admin screen. To configure the page layout, select the "Layout" tab. The layout tab contains two sub tabs, Configuration and Preview. The configuration tab is used to edit the page layout. You can view the changes made to the layout in the Preview tab.

For the purpose of this tutorial, we want to add a label to the layout and display the text "Hello World!" within the page. First we need to add the page layout snippet to the configuration. This section of the configuration is the same for all pages and is the root of a pages configuration.

Select the Configuration section and enter the following config.

````json
{
    "Layout": {
    }
}
````
Adding the above configuration does not do much except define the container that all micro apps will be placed to generate the pages layout. To display the text "Hello World!" within the page, we need to add a label micro app to the pages layout. Lets take a quick look at the micro app configuration for a label.

````json
{
    "View": {
        "Name": "ma-label",
        "Version": "0.0.0-beta.27"
    },
    "DefaultValue": "Hello World!"
}
````

Above is a basic example of a  label micro apps configuration.

* View - The view section of the configuration is standard for all micro apps. It identifies the type and version of a micro app within the page layout.
* DefaultValue - This configuration property is used to define the text that will be displayed within the label.

Add the label configuration to the layout section of the pages configuration. Your page configuration should look similar to the snap below. After entering the information, click the commit changes button.

<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-6.png">

After commiting your changes, select the preview tab to review the layout you just configured.

<img src="https://raw.githubusercontent.com/Schalltech/honeycomb-tutorials/master/tutorials/getting%20started/create%20an%20application/images/create-app-6.a.png">

Success! If everything was configured correctly, you should now see "Hello World!" displayed within the top left corner of the page.

#### Step 6: Styling a micro apps container
So far, we have managed to add a label micro app to the configuration and display the text "Hello World!" within the page. Lets do some basic styling to show the label centered within the page instead of displaying it in the top left corner.

To display the label in the center of the screen, we need to add the below section to the micro apps configuration.

````json
"Container": {
    "display": "flex",
    "flex": "1 1 100%",
    "alignItems": "center",
    "justifyContent": "center"
},
````

Styles defined within the container property will be applied to the container surrounding the micro app. Any valid css value can be specified as log as it is enter in camel case (ex: alignItems vs align-items). 
