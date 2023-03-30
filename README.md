
<h1>**lacework-splunk-addon**</h1>

<b>Version 1.0</b>

A Splunk Technology Add-On (TA) to provide CIM compliance on Lacework alert and audit data. This add-on is designed to work in conjuction with the [Splunk integration](https://docs.lacework.com/onboarding/splunk) available via Lacework UI.

**Installation Notes**<br>

The Splunk TA for Lacework was created for use with the HEC input in Splunk. This contains both Index Time (transforms) and Search Time (props) operations for ingesting and properly sourcetyping the Lacework (HEC) Splunk Alert Channel.

In Splunk Cloud, depending on your deployment type, the HEC endpoint will be similar to  https://http-inputs.<host>.splunkcloud.com:443/<endpoint> and the TA should be deployed here and at the Search Tier.

Do note that the token created on the HEC input needs to match what your Lacework Tenant is configured with, and that the source field in Lacework is set to <b>lacework</b> for the transform to properly identifiy and rename. 

**Installation via Splunk UI**<br>

1. Download the latest release of the add-on from the GitHub repo: https://github.com/lacework-dev/lacework_splunk_addon/releases/new

2. In your Splunk UI, navigate to your **Apps > Manage Apps** page.

![image](https://user-images.githubusercontent.com/79470244/190000321-af73421c-7064-488a-897f-3b4dbc9ab917.png)

3. Click Install App from File.

![image](https://user-images.githubusercontent.com/79470244/190000285-6bdf86e8-b117-498b-8733-a7819351baeb.png)

4. Click **Choose File**. Select the file you downloaded in Step 1.

5. Click **Upload**.

![image](https://user-images.githubusercontent.com/79470244/190000589-14f90817-2608-495e-a934-8d8dc76277be.png)

**Notes**<br>
- This add-on works in conjuction with the existing Lacework integration with Splunk via the UI. This does not replace it.
- In the UI Integration, the "source" field must be set to "lacework" for the TA to properly parse and map fields to CIM. This can be change, but you must rename the props.conf source::lacework stanza appropriately in the app's files.


**Reference URIs**<br>
[Lacework Docs](https://docs.lacework.net)<br>
[Splunk Alert Channel Configuration](https://docs.lacework.com/onboarding/splunk)<br>

