# JIRA Notes Table Generator
Latest version: V 0.6.0 - added more formatting, added formatting for print-table
## Synopsis
This is a webapp that generates a table of issues/tasks from JIRA using the JIRA API for quick meeting notes.

## Motivation
This webapp was created to fulfill the need of quickly creating meeting notes from JIRA and is intended to replace a Excel VBS solution.

## Prerequisites
#### This webapp requires:
- npm
- node.js
- jquery (included)

#### Node.js dependencies (included as zip folders):
- body-parser
- ejs
- express
- jquery.tabulator

## Installation
0. Download node.js and npm; go to https://nodejs.org/en/ to download Node.js and https://nodejs.org/en/download/ to download npm. Administrator privileges will be required.
1. Download the webapp and install the prerequisites; extract the three folders named "jquery-ui", and "node_modules" to their respective folder names inside the webapp's root directory.
2. Run the webapp from a command prompt or terminal; open cmd/terminal, cd  to the webapp directory, and start the webapp using "node server.js" without quotes.
3. The webapp should start on localhost port 8081 (localhost:8081). A different address can be specified by editing server.js. The webapp is default tailored for a custom JIRA so custom fields may differ from other JIRAs.

###Using the Print function
The Print function takes the user to a page containing a simple html table version of the original table which will allow better printing compatibility. To use this, simply press the print button and then print the page using your browser (i.e. Ctrl+P in Chrome).

##Troubleshooting Tips
###ETIMEDOUT
This means that the webapp was unable to connect to the JIRA API. Doublecheck the webapp's internet connection to see if there are any proxies or firewalls blocking the connection.
###JSON.parse error
This means that the returned JSON from JIRA was invalid. This usually means that the username or password you entered was incorrect. The least common reason would be an incorrect URL should the JIRA API ever be changed.

## Built With
This webapp uses a custom modified version of Tabulator to create a table. This modified version includes a Print button that calls for /printpage which is a simplified print friendly page of the table. The original Tabulator can be found here: http://olifolkerd.github.io/tabulator/ and currently is used with an MIT License. A copy of the modified Tabulator and its original License is included in this Github.

## License
This project is licensed under the MIT license. Refer to LICENSE.md for details.
