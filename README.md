# Very simple Asset Service Example

Base for this example is the Predix WebApp Starter project.
Main objective is to provide a lean example that demonstrates the end-to-end integration between the Predix asset service and a web frontend.
This example is not using the asset bootstrap SDK; It is plain Node.js implementation to access assets from the backend service in a Predix-UI (Polymer) frontend.

![](https://github.com/cobra79/predix-webapp-starter/wiki/img/get_engine.png)

## Getting Started

### Get the source code
Make a directory for your project.  Clone or download and extract the starter in that directory.
```
git clone https://github.com/cobra79/predix-webapp-starter.git  
cd predix-webapp-starter
```

### Install tools
If you don't have them already, you'll need node, bower and gulp to be installed globally on your machine.  

1. Install [node](https://nodejs.org/en/download/).  This includes npm - the node package manager.  
2. Install [bower](https://bower.io/) globally `npm install bower -g`  
3. Install [gulp](http://gulpjs.com/) globally `npm install gulp-cli -g`  

### Install the dependencies
Change directory into the new project you just cloned, then install dependencies.
```
npm install
bower install
```

### For this example a real asset-service instance must be used.
Enter the details of your uaa and asset service at least in the localConfig.json 
(to run also the app.js part in the cloud the service information needs to be copied to the manifest)

You need to set:
```
"uaaURL": "https://<your uaa id>.predix-uaa.run.aws-usw02-pr.ice.predix.io",
"base64ClientCredential": "<base 64 encoded client credentials>",
"loginBase64ClientCredential": "<base 64 encoded client credentials>",
...
"assetURL": "https://predix-asset.run.aws-usw02-pr.ice.predix.io",
"assetZoneId": "<your asset zone id>",
...
```

## Running the app locally
The default gulp task will start a local web server.  Just run this command:
```
gulp
```
Browse to http://localhost:5000.
Initially, the app will use mock data for the views service, asset service, and time series service.
Later you can connect your app to real instances of these services.

## Running in Predix Cloud
With a few commands you can build a distribution version of the app, and deploy it to the cloud.

### Create a distribution version
Use gulp to create a distribution version of your app, which contains vulcanized files for more efficient serving.
You will need to run this command every time before you deploy to the Cloud.
```
gulp dist
```

For additional information on the predix-webapp-starter have a look at https://github.com/PredixDev/predix-webapp-starter.

Have a look at  https://github.com/cobra79/predix-webapp-starter/wiki to see simple get and post examples

# Copyright
Copyright &copy; 2015, 2016, 2017 GE Global Research. All rights reserved.

The copyright to the computer software herein is the property of
GE Global Research. The software may be used and/or copied only
with the written permission of GE Global Research or in accordance
with the terms and conditions stipulated in the agreement/contract
under which the software has been supplied.

[![Analytics](https://ga-beacon.appspot.com/UA-82773213-1/predix-webapp-starter/readme?pixel)](https://github.com/PredixDev)

