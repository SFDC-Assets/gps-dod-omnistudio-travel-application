# Travel Request Application
## 1. Description
- This repository contains two travel applications (“Travel Request” and “Travel App”) with related objects and user interface components, approval processes for both apps, sample data for the Travel Request app, and JSON files for the Travel Request app’s related OmniStudio OmniScripts and FlexCards. 
- The main difference between the Travel Request app and the Travel app is that the latter does not feature OmniStudio components, while the former does.
- Both apps were created using a no-code approach and illustrate how Salesforce's declarative tools enable the rapid development of tailored, fully-interactive applications with process automation, analytics, and guided user experiences.
## 2. Disclaimer
- Installation and use of this package is at your own risk. Please consult your organization’s rules and regulations before proceeding.
## 3. Installation & Setup
- The following steps need to be completed in the order listed, to avoid conflicts. 
- Installation takes approximately an hour to complete, depending on your proficiency with Salesforce.
### Set Up OmniStudio Trial Org (Duration: 10 minutes)
1. Successful installation of this package requires a Salesforce org with OmniStudio. If you do not have an existing org with OmniStudio, you can sign up for a free trial version of a Salesforce Public Sector Solutions (PSS) Development org via the following link: https://www.salesforce.com/form/industries/government/public-sector-solutions-learning-trial/
2. For the FlexCards to work properly, a couple of variables will need to be configured:
	- Log in to the trial org.
 	- Click on the Application Launcher to open a list of the org’s applications. The application launcher is located in the top left corner of the screen and is identifiable by nine dots.
	- Type in OmniStudio, and select the OmniStudio app.
	- Select OmniStudio FlexCards from the OmniStudio app’s menu.
	![App Menu](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Advanced%20User%20Details%20-%20Approver%20Settings.png)
	- Click on the warnings button at the top of the screen.
	  ![FlexCard Warning Button](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/FlexCard%20Warnings%20Button.png)
   	- Copy the following two URLs from the dialog box shown: 
		- https://{your domain}/.na225.visual.force.com
		- https://{your domain}.lightning.force.com
  
  		![FlexCard Warnings Modal](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/FlexCard%20Warnings%20Modal.png)
	- Click the gear icon in the upper right corner of the screen and select Setup.
	![Setup Menu Access](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Setup%20from%20Gear%20Icon.png)
	- Type “Remote Site Settings” into the Quick Find search bar and select it.
	![Remote Site Settings Selection](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Quick%20Find%20-%20Remote%20Site%20Settings.png)
	- From the remote site settings page, click on the New Remote Site button.

		![New Remote Site Button](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/New%20Remote%20Site%20Button.png)
	- Add a new remote site.
		- Remote Site Name: EnableLWC
		- Remote Site URL: Copy the url ending in lightning.force.com from the warnings dialog box (e.g. https://appinaday2-pss-mar2023..lightning.force.com)
		- Click the Save and New button.
	- Add another remote site.
		- Remote Site Name: EnableLWCVisual
		- Remote Site URL: Copy the url ending in visual.force.com from the warnings dialog box (e.g. https://appinaday2-pss-mar2023-omnistudio.na225.visual.force.com)
		- Click save.
	- When complete, the remote site settings page should look like this:
	![Remote Site Settings List View](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Remote%20Site%20Settings%20List.png)
	- Return to the OmniStudio FlexCards page of the OmniStudio app. Refresh the page and make sure that the Warnings button is gone.
## Create & Permission a New User (Duration: 15 minutes)
- To support approval process functionality, the Salesforce Development org requires more than one user. Due to the user permissions required for OmniStudio, the easiest method for creating a new user is to clone the original user. “Clone this User” is a free application available on Salesforce’s AppExchange and is native to Salesforce. Using this app will provision the new user with the same permissions, application access, and OmniStudio access as the original user within the PSS Development Org.
- Complete the following steps to install and use this application:
1. Click on the gear icon in the upper right corner of the screen and select Setup.
2. Type “AppExchange” in the Quick Find search bar and select AppExchange Marketplace.
![App Launcher Selection](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Quick%20Find%20-%20AppExchange.png)
3. Click on the AppExchange Home button in the top left corner and select Apps.
![AppExchange App Menu Selection](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/AppExchange%20App%20Search.png)
4. Type “clone this user” in the search bar and select the enter key.
![App Search - Clone This User](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/AppExchange%20Clone%20This%20User%20Search.png)
5. Select the Clone This User tile and click on the Get it Now in the bottom right corner of the screen.
![Clone This User Tile Selection](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/AppExchange%20Clone%20This%20User%20App.png)
6. If prompted, click on the “Open Login Screen” and log into your Development Org.
![Log Into Salesforce Org Screeen](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/AppExchange%20Open%20Login%20Screen%20Modal.png)
7. Click the Allow button to authenticate the org and enable installation.
![Authentication Screen](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/AppExchange%20Allow%20Access%20Modal.png)
8. Select the Install Here button. Do NOT select Install in Sandbox.
![Org Selection Screen](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/AppExchange%20Org%20Selection%20Install%20Modal.png)
9. Select the Checkbox for “I have read and agree to the terms and conditions” and click on the Confirm and Install button.
![Select Checkbox for App Terms](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/AppExchange%20Clone%20This%20User%20Terms%20Modal.png)
10. Click the Install for All Users radio button and then click the Install button. 
![Clone This User Install Wizard](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/AppExchange%20Clone%20This%20User%20Install%20Modal.png)
11. You may receive a message saying that the application is taking too long to install. This is normal. Once the installation is complete you will receive an email saying that it has been installed successfully. 
12. Once installed, access the Salesforce org, and refresh the page. Click on the App Launcher, and type “Clone” in the search box. Select “Clone this User” to open the application.

	![App Launcher App Selection](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/App%20Launcher%20-%20Clone%20This%20User.png)

13. Type your first name into the search box and then select your user to be cloned.
![Clone This User, User Selection](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Clone%20This%20User%20-%20User%20Selection.png)
14. Enter the new user information, leave the default checkbox selections as they are, and click the Save button. 
	- It’s recommended to use your email address for the new user so that you’ll receive the user verification email. Remember that all usernames must be unique. 
	- As an example, you can use the following nomenclature for the cloned user’s username: <firstname>.<last name>.@travelrequestapp.

	![Clone This User, User Creation](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Clone%20This%20User%20-%20New%20User.png)
## Set Up the Manager For the Original User (Duration: 3 minutes)
- For the approval process to work properly, you must assign the new user as your manager. Complete the following steps:
1. Click the avatar in the upper right corner of the screen (it’s an image of a Salesforce mascot) and select the Settings link.
![User Settings Selection](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Avatar%20Dropdown%20-%20Settings.png)
2. Once on the new tab, from the pane on the left of the screen, click Advanced User Details.
![Advanced User Details Selection](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Settings%20-%20Advanced%20User%20Details.png)
3. Click the Edit button at the top of the screen.
![User Edit Button](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Advanced%20User%20Details%20-%20Edit%20Button.png)
4. Scroll down to the Manager field in the Approver Settings section at the bottom of the screen and click the magnifying glass icon.
![User Approver Settings](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Advanced%20User%20Details%20-%20Approver%20Settings.png)
5. Search for and select the second user that you created.
6. Click the Save button at the bottom of the screen.
## Install App Metadata (Duration: 5 minutes)
- The following unlocked package includes two separate travel apps, “Travel Request” and “Travel App”. Please feel free to explore both apps. This Read Me file focuses on configuring the Travel Request app ONLY, as the Travel App does not require any configuration. The Travel App is based on the following Trailhead trail (link).
- To review the differences between the two apps, please refer to the table below:

	**Apps** | **OmniStudio** | **Approval Processes** | **Flow Automation**
	--- | --- | --- | ---
	**Travel Request** | Yes | Yes | Yes
	**Travel App** | No | Yes | Yes
- Complete the following steps to install the metadata (i.e. objects, fields, etc.) for the Travel Request app in your Salesforce instance.
1. Open a new browser window, paste the following URL, and select Enter.
	- https://login.salesforce.com/packaging/installPackage.apexp?p0=04tHr000001VfFIIA0
2. Log into Salesforce with your username and password.
3. Select the Install for All Users radio button. Click the Advanced Options dropdown and select the Compile Only the Apex in the Package radio button, and then click the Install button.
![Install Travel App Modal](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Install%20Travel%20Apps%20Modal.png)
4. The package will begin installing, which should take approximately 1-3 minutes. You will receive an on-screen confirmation and an email when the package has successfully installed. 
5. If installation is taking longer, perhaps due to limited bandwidth, your on-screen notification will reflect this. This is normal.
![Taking Long to Install Modal](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Install%20Travel%20Apps%20-%20Long%20Installation%20Screen.png)
## Activate Flows (Duration: 2 minutes)
- The process automations (Flows) are deployed to your org in an inactive state and must be activated for use. 
1. Click on the gear icon in the upper right corner of the screen and select Setup.
	- If you already have an existing Setup window open, close it and open a new one. When new metadata is added to the org, as in the previous step, it may not be visible in windows that were opened before its installation.
3. Type “flow” in the Quick Find search box and select “Flows” under Process Automation.
4. Scroll down to the “Out of State Travel Flag” flow, select the dropdown on the right side, and click on View Details and Versions.
![Flow Edit Menu](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Flow%20-%20View%20Details%20and%20Versions%20Dropdown.png)
5. In the Flow Versions list, click the “Activate” link.
![Flow Activate Menu](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Flow%20-%20Activate%20Out%20of%20State%20Travel%20Flag%20Flow.png)
6. Repeat steps 3 and 4 for the “Mission Approved” Flow, as needed.
## Configure Path Settings (Duration: 1 minute)
1. Click on the gear icon in the upper right corner of the screen and select Setup.
2. Enter “Path” into the Quick Find search bar and select “Path Settings”.
3. Click the green Enable button. 
![](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Path%20Settings%20-%20Enable.png)
4. The workflow path for Travel Request records is now active.
![](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Path%20Settings%20-%20Active.png)
## Import Travel Request Data (Duration: 5 minutes)
- Upload sample data that can be viewed in list views, reports, dashboards, and OmniStudio components by completing the following steps. The Flex Cards will not work properly without data.
### Download the Data File
1. From the GitHub repository, access the data folder and download the C5ISR-ImportData.csv file to your computer.
![](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/GitHub%20-%20Download%20CSV%20File.png)
### Import the Data
1. Click on the gear icon in the upper right corner of the screen and select Setup.
2. Type “import” in the Quick Find search box and select “Data Import Wizard”.
3. Click the green Launch Wizard button at the bottom of the screen.
4. Click the Custom Objects tab, scroll down the list, and select Travel Requests.
	- It may take a few minutes for new custom objects to appear in the Data Import Wizard after they are added to the org, as they were in a previous step. If you don’t see the Travel Request object available in the list, wait a few minutes, refresh your screen, and search again. Objects may not be listed in alphabetical order.
5. In the middle section, select Add New Records. 
6. In the right section, upload the C5ISR-ImportData.csv file by dragging and dropping it into the upload area, or by clicking the CSV button and following the screen prompts.
![Choose Data Screen](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Data%20Import%20Wizard%20-%20Choose%20Data%20Screen.png)
7. Click the Next button.
8. The metadata from the spreadsheet has already been mapped to the metadata in the Salesforce org, as shown below. Click the Next button.
![Edit Mapping Screen](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Data%20Import%20Wizard%20-%20Edit%20Mapping%20Screen.png)
10. Click the Start Import button.
![Start Import Screen](https://github.com/SFDC-Assets/gps-dod-omnistudio-travel-application/blob/main/images/Data%20Import%20Wizard%20-%20Start%20Import%20Screen.png)
11. Click OK on the confirmation screen. You’ll be redirected to the Bulk Data Load Jobs page where you can monitor the import progress. You’ll receive an email when the job is complete.
