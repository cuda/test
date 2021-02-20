![](RackMultipart20210220-4-1xlfjob_html_8034bf1e99f2aad2.jpg)

PEOPLESOFT SERVERS

DIRECTORY VIEWER

# Project definition: CY2\_DIRECTORY\_VIEWER\_001

![](RackMultipart20210220-4-1xlfjob_html_1ae53f6ad8239008.gif)

Author: E. La Haye

Version: 1.0

Date: 20-02-2021

# Contents

#


[Contents 2](#_Toc64711239)

[1.Version Control 3](#_Toc64711240)

[1.1. Change history 3](#_Toc64711241)

[2.Preface 4](#_Toc64711242)

[2.1. Navigation 4](#_Toc64711243)

[3.Global Design 5](#_Toc64711244)

[3.1. Global design 5](#_Toc64711245)

[4.Technical Description 6](#_Toc64711246)

[4.1. Installation instructions 6](#_Toc64711247)

[4.1.1. Change Assistant approach 6](#_Toc64711248)

[4.1.2. Traditional approach 6](#_Toc64711249)

[4.2. (optional) Add permissions to new permission list 6](#_Toc64711250)

[4.3. (optional) change the delivered menu item navigation 8](#_Toc64711251)

[4.4. (optional) change the delivered message catalog entries 9](#_Toc64711252)

[5.Miscellaneous 10](#_Toc64711253)

[5.1. Other relevant information 10](#_Toc64711254)

1.
# Version Control

  1.
## Change history

| **Date** | **Author** | **Version** | **Changes made** |
| --- | --- | --- | --- |
| 20-02-2020 | E. La Haye | 1 |
 |
|
 |
 |
 |
 |

1.
# Preface

This document describes the installation procedure and options for the PeopleSoft Servers directory viewer functionality.

  1.
## Navigation

This functionality can (by default) be found through navigation: **Root \&gt; CY2 Projects \&gt; PeopleSoft servers directory.**

1.
# Global Design

  1.
## Global design

The &#39;PeopleSoft Directory Viewer&#39; functionality delivers front-end functionality to manage files and directories on PeopleSoft servers for end users.

The functionality consists of:

1. Setup component where administrators can define the permissions available for different directories on the PeopleSoft Servers for end users.
2. Viewer component where end users can manage files and directories on the PeopleSoft Servers.

**Common uses:**

The functionality is commonly used to:

1. Allow developers access to log files on the application server and web server for debugging errors and viewing integration logs.
2. Allow end users the ability to upload and delete files to / from specific directories that can be used as upload directories for business transactions that require external files (csv / excel / etc.).
3. ![](RackMultipart20210220-4-1xlfjob_html_89923662261f98a0.gif)Allow admins easy access for server directories while using the front-end application.

A word of caution: working with PeopleSoft servers means working with the real server directories that are necessary to keep the PeopleSoft environment running. Any file transaction that end users can perform cannot be undone. Delete is Delete!

The functionality can safely be used in a production environment if and when you have clearly defined which end users can perform which file transactions in which directories.

1.
# Technical Description

  1.
## Installation instructions

For the installation of the &#39;PeopleSoft Directory Viewer&#39; functionality the following steps need to be taken:

    1.
### Change Assistant approach

Load the change package updCY2\_DIRECTORY\_VIEWER\_001 into the database using Change Assistant.

    1.
### Traditional approach

In case you don&#39;t want to use the change assistant to load the project:

1. Open the updCY2\_DIRECTORY\_VIEWER\_001 package and load the project located in the folder &quot;CY2\_DIRECTORY\_VIEWER\_001&quot; into the database.
2. Open the updCY2\_DIRECTORY\_VIEWER\_001 batch folder located in the updCY2\_DIRECTORY\_VIEWER\_001 package and load the message catalog entries through data mover using the .DAT files in the &quot;data&quot; folder and the DMS script in the &quot;scripts&quot; folder.
3. Build the tables and views contained in the project (create tables, create views).

  1.
## (optional) Add permissions to new permission list

Optionally you can add the following menu items to a relevant permission list:

1. CY2\_PSS\_DIR\_MENU

Maintain permission lists through navigation: **PeopleTools \&gt; Security \&gt; Permissions &amp; Roles \&gt; Permission Lists.**

The permission list as shown below is delivered with the project but does not have to be used.

![](RackMultipart20210220-4-1xlfjob_html_a7e7f748a6c39206.gif)

The following menu is defined in the permission list.

![](RackMultipart20210220-4-1xlfjob_html_76703a43f4f8b69a.gif)

![](RackMultipart20210220-4-1xlfjob_html_e055c16342539f64.gif)
The following components are autorised in the menu.

  1.
## (optional) change the delivered menu item navigation

By default the &#39;PeopleSoft Directory Viewer&#39; functionality can be reached through navigation: **Root \&gt; CY2 Projects \&gt; PeopleSoft servers directory .**

![](RackMultipart20210220-4-1xlfjob_html_e1a5bdca6f89d8d7.gif)
If needed these menu items can be moved elsewhere by altering the &#39;structure and content&#39; portal registry that can be reached through navigation: **PeopleTools \&gt; Portal \&gt; Structure and content**

  1.
## (optional) change the delivered message catalog entries

There are 48 message catalog entries delivered with the project, all using message catalog: 25301.

Those can be altered through the following navigation: **PeopleTools \&gt; Utilities \&gt; Administration \&gt; Message Catalog**.

Or alternatively can be altered by changing the DAT file delivered as part of the project.

1.
# Miscellaneous

  1.
## Other relevant information

Functional and technical documentation for this project are described in two other documents that are delivered as part of the change package (folder documentation).

|
 | CY2 IT Services |
 |
| --- | --- | --- |
