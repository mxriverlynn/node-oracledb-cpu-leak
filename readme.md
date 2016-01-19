# App To Demo node-oracledb CPU Leak / Spike

This app is nothing more than a base Express.js install, with node-oracledb
creating a single connection in the bin/www file. Other than adding this
connection, there is nothing more than what comes out of the express generator
in this project.

Environment: 

* OSX v10.11.3
* Node v4.2.2
* NPM v2.14.7
* Oracle 11g

To reproduce the CPU spike / leak on OSX 10.11.3, follow these steps:

0. edit `dbconfig.json` to supply your connection info
0. `npm install`
0. `node bin/www`
0. After the app starts, press ctl-c once
0. Watch the CPU spike, forever
