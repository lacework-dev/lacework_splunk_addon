# lacework-splunk-addon
A Splunk TA to provide CIM compliance on Lacework alert and audit data. This add-on is designed to work in conjuction with the [Splunk integration](https://docs.lacework.com/onboarding/splunk) available via Lacework UI.

# Installation

## Installation via Splunk UI

1. Download the latest release of the add-on from the GitHub repo: https://github.com/lacework-dev/lacework_splunk_addon/releases/new

2. In your Splunk UI, navigate to your **Apps > Manage Apps** page.

![image](https://user-images.githubusercontent.com/79470244/190000321-af73421c-7064-488a-897f-3b4dbc9ab917.png)

3. Click Install App from File.

![image](https://user-images.githubusercontent.com/79470244/190000285-6bdf86e8-b117-498b-8733-a7819351baeb.png)

4. Click **Choose File**. Select the file you downloaded in Step 1.

5. Click **Upload**.

![image](https://user-images.githubusercontent.com/79470244/190000589-14f90817-2608-495e-a934-8d8dc76277be.png)

# Notes
- This add-on works in conjuction with the existing Lacework integration with Splunk via the UI. This does not replace it.
- In the UI Integration, the "source" field must be set to "lacework" for the TA to properly parse and map fields to CIM. This can be change, but you must rename the props.conf source::lacework stanza appropriately in the app's files.
