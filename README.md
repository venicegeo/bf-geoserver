## Beachfront GeoServer

In cases where a GeoServer service tile is not available for Beachfront, this script can be used to stand up an app called `bf-geoserver` in a PCF environment for use. Simply run the JenkinsFile to push the application and create a PCF CUPS service if needed. 

## Running as an App

This is not a PCF service and it is not intended to replace a service tile long-term. As an app, any restages or redeploys will *delete any state on disk* including the GeoServer data directory. Do not restage the app without understanding that the data directory will be deleted upon restage. If this get restaged, just restart `pz-access` followed by `bf-api` to re-create the GeoServer state. 
