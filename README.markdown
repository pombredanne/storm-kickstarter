# BASE STORM PROJECT

Collection of basics tools to create your storm project

---

Table of Contents

* <a href="#getting-started">Getting started</a>
* <a href="#maven">Using storm-starter with Maven</a>

---


<a name="getting-started"></a>

# Getting started

## Prerequisites

First, you need `java` and `git` installed and in your user's `PATH`.

Next, make sure you have the storm-kickstarter code available on your machine.  Git/GitHub beginners may want to use the
following command to download the latest storm-starter code and change to the new directory that contains the downloaded
code.

    $ git clone https://github.com/lluiscanet/efruti.git && cd storm-starter



If you want to learn more about how Storm works, please head over to the
[Storm project page](http://github.com/nathanmarz/storm).


# Using storm-kickstarter with Maven

## Install Maven

[Maven](http://maven.apache.org/) Install Maven (preferably version 3.x) by following
the [Maven installation instructions](http://maven.apache.org/download.cgi).


## Running topologies with Maven

storm-starter contains [pom.xml](pom.xml) which can be used with Maven using the `-f` option. For example, to
compile and run `WordCountTopology` in local mode, use the command:

    $ mvn compile exec:java -Dstorm.topology=com.dadrin.storm.kickstarter.MyTopology

## Packaging storm-starter for use on a Storm cluster

You can package a jar suitable for submitting to a Storm cluster with the command:

    $ mvn package

This will package your code and all the non-Storm dependencies into a single "uberjar" at the path
`target/


## Running unit tests

Use the following Maven command to run the unit tests that ship with storm-starter.  Unfortunately `lein test` does not
yet run the included unit tests.

    $ mvn pom.xml test

