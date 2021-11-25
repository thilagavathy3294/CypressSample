# CypressSample

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See **Setup notes** on how to import the project on your system.

### Prerequisites

* Node js
* Visual studio code

### Installing -

A step by step series of examples that tell you how to get the package installed and running

**Node js:**
1. Download the Node js from 'https://nodejs.org/en/download/' and install in your local machine.

**Visual studio code:**

1. Download the latest visual studio code from 'https://visualstudio.microsoft.com/'

## Running the tests

### From Visual Studio code

1. Create a new folder with the project name and open the project in Visual Studio code.
2. Got to Terminal--> click on ' New Terminal'
3. To initiate node type 'npm init' in terminal
4. To install cypress type 'npm install cypress --save-dev' 
5. Create the Cypress script in 'todo-spec.js' and it has renamed here 'Sample.spec.js'.
6. To open type 'npx cypress open' or 'node_modlues/.bin/cypress open' in terminal.
7. Cy Window will open and click on the 'Sample.spec.js' to execute the script.

**Report Generation:**
1. In terminal type 'npm i --save-dev cypress-mochawesome-reporter'
2. Setup  the following dependencied in cypress.json
"reporter":"cypress-mochawesome-reporter",
    "reporterOptions":{
    "reportDir":"cypress/report",
    "reportFilename":"report",
    "overwrite":true,
    "html":true,
    "json":true,
    "timestamp":"mmddyyyy_HHMMss",
    "charts": true,
    "reportPageTitle":"MyTest",
    "embeddedScreenShots":true,
    "inlineAssets":true
    }
3. Setup the following under plugin/index.js
module.exports = (on, config) => {
  require('cypress-mochawesome-reporter/plugin')(on);
}
4. Add the following Import in support/index.js
import 'cypress-mochawesome-reporter/register'
5.To generate report type 'npx run cypress'
6.Get the reports under 'report' folder.


### Repo owner or admin

* **Admin:** Thilagavathy

## QA developers

* [**Thilagavathy**](mailto:k.pthilagavathy@gmai.com)
