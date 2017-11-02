# queue2file
Simple Mule Application for transferring a file from queue to a File

# Problem:
org.mule.module.launcher.DeploymentStartException: ClassNotFoundException: org.apache.activemq.ActiveMQConnectionFactory

# Solution Procedure:

**For Maven Users,**
---

If your application is mavenized, then go to POM file and add the following dependency:

    <dependency>
        <groupId>org.apache.activemq</groupId>
        <artifactId>activemq-all</artifactId>
        <version>5.14.5</version>
    </dependency>
 
**For gradle users,**
---

If your application is gradlized, then go to **build.gradle** and add the following dependency:

> // https://mvnrepository.com/artifact/org.apache.activemq/activemq-all

> compile group: 'org.apache.activemq', name: 'activemq-all', version: '5.14.5'

**For Others,**
---

If your application is not mavenized, then

1. Right click on your project
2. click on Properties and in the properties window,
3. click/select Java Build Path and select the tab Libraries and
4. click on the button Add external JARS.. and
5. select file activemq-all-x.xx.x,jar
6. which will be available in the root folder of the apache-activemq folder.

Resource Link:

1. [Resolve ActiveMQConnectionFactory class not found exception](http://www.tips.sentientmindz.com/2016/09/04/activemqconnectionfactorycnf/)
2. https://forums.mulesoft.com/questions/38918/week-5-exception-on-activemq-could-you-please-help.html

