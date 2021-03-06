---

copyright:
  years: 2017, 2018
lastupdated: "2018-09-25"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Customizing the cluster using a customization script

To enable an application to connect to {{site.data.keyword.cos_full_notm}}, you must update the {{site.data.keyword.iae_full_notm}} cluster configuration file (core-site.xml file) to include Cloud Object Storage credentials and other required connection values.

One way of doing this is to use a customization script to configure the properties that need to be updated in the core-site.xml file. It uses the Ambari configs.py file to make the required changes.

This [customization sample script](https://github.com/IBM-Cloud/IBM-Analytics-Engine/blob/master/customization-examples/associate-cos.sh) configures the {{site.data.keyword.iae_full_notm}} cluster with HMAC authentication parameters. The example shows the complete source code of the customization script. You can modify the script for IAM authentication style parameters. The sample restarts only the affected services and, instead of sleeping for a long random interval after firing the Ambari API, the progress is polled via the Ambari API.
