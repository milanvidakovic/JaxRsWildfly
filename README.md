# JaxRsWildfly demo of the JaxRs interceptor

This is JBoss Wildfly-based demo of the Authentication and Authorization framework.
See source of the interceptor at [Github](https://github.com/milanvidakovic/JaxRsInterceptor).

In the WEB_INF/lib you will find the interceptor as agent.jar file.

In the WEB_INF/lib you will also find AspectJ files that this interceptor uses:
* aspectjweaver-1.9.6.jar
* aspectjrt-1.9.6.jar
* aspectjtools-1.9.6.jar

Add at the end of VM params: 

```
-Djboss.modules.system.pkgs=org.jboss.byteman,org.jboss.logmanager -Djava.util.logging.manager=org.jboss.logmanager.LogManager -javaagent:<path-to-aspectj>/aspectjweaver-1.9.6.jar
```

Add following jars to the `Servers -> Wildfly Runtime Server -> Open launch configuration -> Class Path -> User Entries`:
* <WILDFLY_HOME>/modules/system/layers/base/org/jboss/logmanager/main/jboss-logmanager-(version).jar
* <WILDFLY_HOME>/modules/system/layers/base/org/jboss/log4j/logmanager/main/log4j-jboss-logmanager-(version).jar    
