# Jenkins-Guide

It's an open source continuous integration / continuous delivery and development automation software DevOps tool written in the JAva programming language. It's primarily used to implement CI/CD workflows, called pipelines. But what are pipelines?

A continuous delivery pipeline is an implementation of the continuous paradigm, where automated builds, tests and deployments are orchestrated as one release workflow. Put more plainly, a CD pipeline is a set of steps your code changes will go through to make their way to production.

#### Commands 

start<br>
<i>brew services start jenkins-lts</i>

restart <br>
<i>brew services restart jenkins-lts</i>

stop <br>
<i>brew services stop jenkins-lts</i>

### Project functions

- Upstream projects - Are projects which trigger other projects. This means that a project will be executed but only if the build sucesses.
