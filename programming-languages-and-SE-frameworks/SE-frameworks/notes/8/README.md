# Continuous integration

## System building

* When a software is released we must build a package for production
  * Nowadays, containers are more common
* Performing the release process manually can be error prone.
  * Sometimes, it requires specific members or a release team to
    perform.
* When we build onto a new machine, we want to perform as few manual
  steps as possible to reduce risk.
* We could write automated scripts to perform the steps for us.
* Build automation tools help up to make building fast and consistent.

## Build automation

* Build automation tools can perform:
  * Downloading external dependencies
    * Projects require external libraries be it frameworks or utility
    * We may also vendor / version control libraries
    * Package managers are used to handle package repositories from a
      central hub.
    * Build tools will use package managers to get the required
      dependencies before building.
  * Deciding which source files need compiling
  * Compile into single executable
  * Change parameters for compilation to different environments
  * Run automated tests
  * Deploy to production

## Continuous integration

Is the agile practise of integrating all developer's code into a shared
branch.

It is common practise to automatically build verify and deploy the code
to a staging environment with each commit to develop on a nightly basis.
The regular building provides developer confidence to know that the most
current version of the code is functional.

### Advantages

* Allows for code to be tested and build on a fixed schedule which will
  feedback bugs to developers.
* With good unit tests, continuous integration can provide a high level
  of confidence in the software.
* Broken development build should be fixed as a matter of priority so
  that other developers are not held up.
* Working snapshots can allow regular delivery to project stakeholders

### CI/CD tools

CI/CD tools provides a graphical interface which handles the CI/CD
workflow. This saves time because common steps are provided without
requiring time to manually create common features.

Easier to standardize workflow across and organisation and other
projects.

### Containers

Containers is an virtual machine image. Contains everything required to
run the application including the operating system and libraries.

Containers are machine agnostic and which means that they can be
deployed to different machines easily.


