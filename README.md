ISAAC-DB
========

A project for creating an ISAAC Database with the desired dataset

There are current three example sub-projects, which each build a different combination of data into ISAAC.

You can either go to the sub-directory and execute the desired build, or you can run them as a profile from 
this directory.

The current profiles are:

-P solor-all
-P sct-loinc
-P sct

For either method of execution - use the following maven commands:

To just build the DB:

`mvn clean compile`

This will create the DB in the project-specific sub-folder {build-config}/target/[descriptive-name].bdb

To create the DB, and also create a zip package of the DB, run:
	
`mvn clean package`

When you are happy with the resulting database - to publish it to an archiva server assemble a command along the lines of:

`mvn clean deploy -DaltDeploymentRepository=maestro::default::https://va.maestrodev.com/archiva/repository/data-files/`
