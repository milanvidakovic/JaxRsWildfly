# JaxRsWildfly demo of the JaxRs interceptor

This is JBoss Wildfly-based demo of the Authentication and Authorization framework.
See source of the interceptor at [Github](https://github.com/milanvidakovic/JaxRsInterceptor).

In the WEB_INF/lib you will find the interceptor as agent.jar file.

In the WEB_INF/lib you will also find AspectJ files that this interceptor uses:
* aspectjweaver-1.9.6.jar
* aspectjrt-1.9.6.jar
* aspectjtools-1.9.6.jar

You also need to modify Wildfly startup by adding the following to the VM arguments:
```
-Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.util.logging.manager=org.jboss.logmanager.LogManager -javaagent:c:\apache-tomcat-7.0.94\lib\aspectjweaver-1.9.6.jar
```
