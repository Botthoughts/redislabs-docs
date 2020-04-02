---
Title: Database Access Control
description:
weight: $weight
alwaysopen: false
categories: ["RS"]
---
To make it easy to work with Redis Enterprise Software (RS) databases from the start,
there are no default security requirements for clients to send commands to the database.
The database does not require clients to authenticate, and it does not restrict the client to running only authorized commands on particular keys.
In many deployments, the authentication and authorization are managed by other application components
so that this open communication is not a security risk.

RS lets you control access to the database with:

- Authentication - Only authenticated users can access the database
- Authorization - Users can only run specific commands on specified keys as defined by configured ACLs

With a [Redis ACL](https://redis.io/topics/acl) you can define the commands that a user can run and on which keys the commands can be used.
For example, if you want a user to only use the `get` command on keys that begin with status, you can create an ACL rule of `+get ~status*`.

Cluster admins define these ACL rules and name them. Then cluster members and DB members can add roles to a database and assign the ACL to the role. As a result, the ACL applies to any user that is a member of the role and restricts the commands that the user can run on that database.

To add a role with ACLs to a database:

1. In the Access control list section of the database configuration, click [Add](/images/rs/icon_add.png#no-click "Add").
1. Select the role that you want to have access to the database.
1. Select the ACL that you want the role to have in the database.
1. Click ![Save](/images/rc/icon_save.png#no-click "Save") to save the access control rule.
1. Click **Update** to save the changes to the database.
