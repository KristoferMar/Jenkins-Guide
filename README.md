# Jenkins-Guide

It's an open source continuous integration / continuous delivery and development automation software DevOps tool written in the Java programming language. It's primarily used to implement CI/CD workflows, called pipelines. But what are pipelines?

A continuous delivery pipeline is an implementation of the continuous paradigm, where automated builds, tests and deployments are orchestrated as one release workflow. Put more plainly, a CD pipeline is a set of steps your code changes will go through to make their way to production.

<h2>Jenkins benefits</h2>
- Jenkins provides a feedback loop back to the developer to fix build errors <br>
- Research has shown that it's a lot quicker to have a developer fix the error immediatly (when the code is still fresh in memory) <br>
- Jenkins can publish every build of your software <br>
- This build already has gone through automated testing <br>
- When published and deployed to a dev/qa/staging server, you can advance the Software development lifecycle (SDLC) much quicker <br>
- The quicker you can go through an iteration of the SDLC the better <br>

<h1>Jenkins setup</h1>

Get initial AdminPassword to "unlock jenkins" 
<pre>
  cat /var/jenkins_home/secrets/initialAdminPassword
</pre>

#### Jenkins + brew commands

List of brew services to find jenkins <br>
<i> brew services list </i>

start<br>
<i>brew services start jenkins-lts</i>

restart <br>
<i>brew services restart jenkins-lts</i>

stop <br>
<i>brew services stop jenkins-lts</i>

### Project functions

- Upstream projects - Are projects which trigger other projects. This means that a project will be executed but only if the build sucesses.
- Downstream projects - Are projects which are triggered by other projects. They only trigger when another projects is compleated. 

## Jenkins Build

### Jenkins build periodically

build periodically does what it says. Link with details can be found below: <br>
https://www.lenar.io/jenkins-schedule-build-periodically/

<h2>Jenkins roles</h2>
<h3>Check if admin</h3>
Under the "jenkins" tab you can verify if you are admin by looking for the "Manage Jenkins" option. If the option is not visible you are not admin.

<h2>Jenkins scripting</h2>
It's possible to create jenkins pipelines using groovy scripting and it is a much more effecient way to create pipelines once you learn how to do it. <br>
Jeg need to down load the "jenkins job DSL" plugin to be able to use it.<br>

<h2>Jenkins secutiry</h2>

If you lock yourself out or need to force a way in you can edit the jenkins config.xml file if you have access to it. <br>

<pre>
docker stop jenkins
# edit /var/jenkins_come/config.xml
docker start jenkins
</pre>

From here you have two options you can <br>
1. 
<pre>
Make sure you have:
useSecurity>false /useSecurity>

And remove all:
authorizationStrategy> references
</pre>

2. 
<pre>
authorizationStrategy> class="hudson.security.ProjectMatrixAuthorizationStrategy"> 
  permission>hudson.model.Hudson.Administer:YOUR-USER /permission>
/authorizationStrategy>
</pre>
<h1>Guides</h1>

https://coralogix.com/blog/how-to-install-and-configure-jenkins-on-the-mac-os/
