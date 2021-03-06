# Swagger Sample App

## Overview
This is a java project to build a stand-alone server which implements the Swagger spec.  You can find out more about both the spec and the framework at http://swagger.io.  

### To run (with Maven)
To run the server, run this task:
<pre>
mvn package -Dlog4j.configuration=file:./conf/log4j.properties jetty:run
</pre>

This will start Jetty embedded on port 8002.

### Testing the server
Once started, you can navigate to http://localhost:8002/api/swagger.json to view the Swagger Resource Listing.
This tells you that the server is up and ready to demonstrate Swagger.

### Using the UI

The sample application hosts the [swagger-ui](https://github.com/swagger-api/swagger-ui) at http://localhost:8002. You can use that to browse the API.

### Applying an API key
The sample app has an implementation of the Swagger ApiAuthorizationFilter.  This restricts access to resources based on api-key.  There are two keys defined in the sample app:

<li>- default-key</li>

<li>- special-key</li>

When no key is applied, the "default-key" is applied to all operations.  If the "special-key" is entered, a number of other resources are shown in the UI, including sample CRUD operations.  Note this behavior is similar to that on http://developer.wordnik.com/docs but the behavior is entirely up to the implementor.