# lacework-splunk-addon
A TA to provide CIM compliance on Lacework alert and audit data

Please note this add-on is FIELD-developed and is a work in progress until API and logging updates have been made.

These knowledge objects are dependent on the "source" field in the Lacework Platform's alert channel configuration being named "lacework".
This can be edited, but you must rename the props.conf source::lacework stanza appropriately.