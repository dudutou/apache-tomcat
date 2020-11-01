# apache-tomcat
The demo for studying apache -> tomcat connectors using docker.

## Which connector: mod_jk or mod_proxy?
* See: https://cwiki.apache.org/confluence/display/TOMCAT/Connectors

## Using mod_proxy
* docker-compose -f docker-compose-mod_proxy.yml up
* Action: access this url: http://localhost/tomcat/sample/
* Result: you will get the response from the tomcat server containers(my-tomcat-1/my-tomcat-2), and also load balanced between the two.

## Using mod_jk
* docker-compose -f docker-compose-mod_jk.yml up
* Action: access these urls: http://localhost/tomcat/sample/ http://localhost/SampleWebApp/SnoopServlet
* Result: you will get the response from the tomcat server containers(my-tomcat-1/my-tomcat-2), and also load balanced between the two.
