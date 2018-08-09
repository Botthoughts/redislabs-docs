---
Title: Managing Cluster Alerts in Redis Enterprise Software (RS)
description: $description
weight: $weight
alwaysopen: false
---
The **Settings \> Alerts** allows you to designate which cluster-level
events trigger alert notifications.

**Note**: For instructions on configuring alerts at the database level,
refer to [Database
alerts](/redis-enterprise-documentation/database-configuration/database-alerts).

Certain alerts, such as **Node failed** can only be turned on or off.
Some alerts require setting a threshold, such as **Node memory has
reached a certain percentage of its capacity**.

Configured alerts appear in the relevant **Cluster **or **Node
Status** fields, in the **Log **page, and can also be sent via email.

To enable receiving email alerts:

1.  Select the checkbox at the bottom of the Alerts page.
2.  Add the relevant users to the Team page, and ensure that the
    checkbox Email Alerts is selected (for additional details, refer to
    [Managing
    users](/redis-enterprise-documentation/administering/cluster-operations/settings/account-management/)).
3.  Configure the email server settings on the General page (for
    additional details, refer to [Managing general
    settings](/redis-enterprise-documentation/administering/cluster-operations/settings/general/)).