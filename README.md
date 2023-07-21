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

