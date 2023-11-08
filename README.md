Node-RED on Code-Engine
====================================

### Customising Node-RED

This repository is here to be cloned, modified and re-used to allow anyone create
their own Node-RED based application that can be quickly deployed to IBM Cloud Code Engine.

The default flows are stored in the `defaults` directory in the file called `flow.json`.
When the application is first started, this flow is copied to the attached Cloudant
instance. When a change is deployed from the editor, the version in cloudant will
be updated - not this file.

The web content you get when you go to the application's URL is stored under the
`public` directory.

Additional nodes can be added to the `package.json` file and all other Node-RED
configuration settings can be set in `bluemix-settings.js`.

### Environment Variables

The following environment variables can be used to configure the application:

 - `NODE_RED_STORAGE_NAME` - the Cloudant service name as exposed in Resource List of your Cloudant Account
 - `NODE_RED_STORAGE_DB_NAME` - the name of the database to use on Cloudant (create a db using the Cloudant Dashboard)
 - `NODE_RED_STORAGE_DB_URL` - the url of the Cloudant database you can retrieve from Service Credentials
 - `NODE_RED_STORAGE_APP_NAME` - the prefix that will be used in the DB to identify flows
 - `NODE_RED_USERNAME`, `NODE_RED_PASSWORD` - if set, used to secure the editor
 - `NODE_RED_GUEST_ACCESS` - if the editor is secured, this will allow anonymous,
    read-only access
 - `NODE_RED_USE_APPMETRICS` - enables the appmetrics dashboard
