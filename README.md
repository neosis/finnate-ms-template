# Centelon Finnate Microservice Template 

[comment]: <> ([![Build Status]&#40;https://api.travis-ci.com/apache/fineract-cn-template.svg?branch=develop&#41;]&#40;https://travis-ci.com/apache/fineract-cn-template&#41;)

This project provides a template layout for all Centelon's Finnate Microservices.

## Abstract
Finnate suite of products by Centelon

## Steps needed to turn the template project into a real project

1.  Git clone template into {project name} folder

        git clone https://github.com/neosis/finnate-ms-template.git {project name}

2.  Delete _.git_

        rm -rf .git
    
3.  Open settings.gradle and replace value of _rootProject.name_ with {project name}

4.  Open root build.gradle and replace value of _version_ with 0.1.0-snapshot

6.  Create Gradle wrapper

        gradle wrapper

6.  Open all module specific build.gradle files (api, service, and component-test) and replace value of _group_ with com.centelon.finnate.{project name}

7.  Import project into IDE

8.  Rename all com.centelon.finnate.template packages to com.centelon.finnate.{project name}

9.  Open _SampleRestConfiguration_ and _SampleServiceConfiguration_, adjust @ComponentScan to reflect the new package name

10. Open _application.yml_ and replace _server.contextPath_ with /{project name}/v1/*

11. Open _bootstrap.yml_ and replace _spring.application.name_ with {project name}/v1/

12. Open _SampleTest_ and replace constructor argument of TestEnvironment in line 80 with {project name}/v1/

13. Run _SampleTest_

14. Replace the contents of the README with text describing your new project.

15. Happy coding! ; o) 

[comment]: <> (16. For Travis-ci.com continuous integration server to start uploading artifacts to Artifactory)

[comment]: <> ( you need to put into .travis.yml a password that is encrypted with public key of https://travis-ci.com/apache/fineract-cn-newRepositoryNameInGithub)

[comment]: <> (See [project wiki]&#40;https://cwiki.apache.org/confluence/display/FINERACT/Fineract+CN+Project+Structure&#41;.)


## Versioning
The version numbers follow the [Semantic Versioning](http://semver.org/) scheme.

In addition to MAJOR.MINOR.PATCH the following postfixes are used to indicate the development state.

* BUILD-SNAPSHOT - A release currently in development. 
* M - A _milestone_ release include specific sets of functions and are released as soon as the functionality is complete.
* RC - A _release candidate_ is a version with potential to be a final product, considered _code complete_.
* RELEASE - _General availability_ indicates that this release is the best available version and is recommended for all usage.

The versioning layout is {MAJOR}.{MINOR}.{PATCH}-{INDICATOR}[.{PATCH}]. Only milestones and release candidates can  have patch versions. Some examples:

1.2.3.BUILD-SNAPSHOT  
1.3.5.M.1  
1.5.7.RC.2  
2.0.0.RELEASE

[comment]: <> (## License)

[comment]: <> (See [LICENSE]&#40;LICENSE&#41; file.)
