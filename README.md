WfsGeoServer251
===============

This GeoServer 2.5.1 configuration has the GML Application Schema Extension and accepts WFS HTTP requests.  Download it and push it to a Red Hat OpenShift TomCat 7 Cartridge! Or, download it for a machine installation.

Try a live OpenShift instance at https://geoserver-gmoyano.rhcloud.com/geoserver251

The GML Application Schema Extension leverages the WFS (http://en.wikipedia.org/wiki/Web_Feature_Service) implemention provided by GeoServer.

A helpful post to reference for placing the download in the right place for a machine installation is the following:

http://stackoverflow.com/questions/651038/how-do-you-clone-a-git-repository-into-a-specific-folder

After placing the files in the right place, make sure file permissions are set so that the Tomcat service can appropriately access the files.

Also, ensure the following minimum Java values and session variables are appropriately set to provide the instance the resources it needs to run:

JAVA_OPTS="-server -Xms48M -Xmx256M -XX:MaxPermSize=128M -DGEOSERVER_HOME=/usr/share/tomcat/webapps/wfsgeoserver -DGEOSERVER_DATA_DIR=/usr/share/tomcat/webapps/wfsgeoserver/data_tutorial_appschema"

-g
