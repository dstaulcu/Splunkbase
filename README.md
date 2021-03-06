Synopsis:
-----------------------------------
[Python script](https://github.com/dstaulcu/Splunkbase/blob/main/get-splunkapps-ext.py) to maintain [local copy](https://github.com/dstaulcu/Splunkbase/blob/main/splunkbase_catalog.csv) of Splunkbase application catalog.

![alt text](https://github.com/dstaulcu/Splunkbase/blob/main/demo.gif)

Notes:
-----------------------------------
Splunk.com provides an [API](https://splunkbase.splunk.com/api/v1/app) that allows you to export a list of apps available on Splunkbase.  Exported lists of apps can be uploaded as lookups into Splunk instances that are not connected to the Internet. You can compare output of the [apps API](https://docs.splunk.com/Documentation/Splunk/8.2.6/RESTREF/RESTapps) on splunk servers to an imported splunkbase application catalog lookup file to determine if apps installed on the server have updates available.  This alone is useful for app update planning.

If you are planning a Splunk Enterprise update, it would also be helpful understand additional details about apps such as their compatability with varying Splunk versions and CIM data models.  This script scrapes additional information of interest from each app's  web page and includes extended information in the application catalog CSV file.  Additional fields include app version, app download filename, supported splunk versions, and supported cim versions.
