WfsGeoServer251
===============

This GeoServer 2.5.1 instance is configured with a GML Application Schema extension and accepts WFS HTTP requests.  GeoServer is a reference implementation of the WFS specification [ http://en.wikipedia.org/wiki/Web_Feature_Service ].  

Try It Live!
------------
A live instance is on OpenShift [ https://geoserver-gmoyano.rhcloud.com/geoserver251 ].  (Note: Please allow 1-3 minutes to start the service.  Your browser may appear to hang while the service is spinning up.)

Discover the capabilities provided by this WFS instance:

    https://geoserver-gmoyano.rhcloud.com/geoserver251/wfs?service=wfs&version=2.0.0&request=GetCapabilities

Request a sample Feature (http://en.wikipedia.org/wiki/Geography_Markup_Language#Features):

    https://geoserver-gmoyano.rhcloud.com/geoserver251/wfs?service=wfs&&version=2.0.0request=GetFeature&typeName=gsml:MappedFeature

Clone It!
---------
Clone the repository [ https://github.com/gmoyanollc/WfsGeoServer251 ] for this instance and run it in a traditional machine installation or your own OpenShift environment.

First, download git if you don't already have it.

Next, clone the repository 

    git clone https://github.com/gmoyanollc/WfsGeoServer251.git

The following is a helpful reference for placing the git in the right place for a machine installation:

  http://stackoverflow.com/questions/651038/how-do-you-clone-a-git-repository-into-a-specific-folder

To run this instance in your own OpenShift environment, perform the git remote add, merge, and push commands [  http://stackoverflow.com/questions/12657168/can-i-use-my-existing-git-repo-with-openshift/12669112#12669112 ].

After placing the files in the right place, make sure file permissions are set so that the Tomcat service can appropriately access the files.

Also, ensure the following minimum Java values and session variables are appropriately set to provide the instance the resources it needs to run:

  JAVA_OPTS="-server -Xms48M -Xmx256M -XX:MaxPermSize=128M -DGEOSERVER_HOME=/usr/share/tomcat/webapps/wfsgeoserver -DGEOSERVER_DATA_DIR=/usr/share/tomcat/webapps/wfsgeoserver/data_tutorial_appschema"

Run It!
-------
Access a local GeoServer instance at http://localhost:8080/wfsgeoserver .

Log in to GeoServer as "root".  The password is located in the following file:

  WebAppHome "/wfsgeoserver/data_tutorial_appschema/security/masterpw.info"

GeoServer logging is located in the following file:

  WebAppHome "/geoserver/data_tutorial_appschema/logs/geoserver.log"

Finally
-------
I hope this helps.  Let me know how it goes.
//

