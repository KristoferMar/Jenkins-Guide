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



