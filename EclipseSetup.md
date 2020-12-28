# Recommended Eclipse Setup

If you do not have an existing Eclipse setup, StarChart Labs recommends starting from bare-bones, to avoid unnecessary plug-ins cluttering the UI and startup. This guide is intended to reflect the steps necessary to create a functioning Eclipse environment.

This guide was last altered based on a full test setup with the latest 2019 version of Eclipse.

# General Installation

Download the [Runtime Binary](http://download.eclipse.org/eclipse/downloads/#PlatformRuntime). Choose the entry for the OS under the "Platform Runtime Binary" Heading. This installs Eclipse without any plug-ins by default, allowing greater customization
After downloading, install the following via the update site installation method (Help -> Install New Software). The below is of the format (Update Site -> Group -> Feature)
- (Eclipse release name)
  - Collaboration
    - Eclipse Git Team Provider
  - General Purpose Tools
    - Marketplace Client
  - Programming Languages
    - Eclipse Java Development Tools
    - JavaScript Development Tools
  - Web, XML, Java EE and OSGi Enterprise Development
    - Eclipse Faceted * (All features which start with Eclipse Faceted)
    - Eclipse Java Web Developer Tools
    - Eclipse Web Developer Tools
    - JST Server Adapters
    - JST Server Adapters Extensions

Finally, install the "Buildship Gradle Integration" Plug-in and "Test NG" plug-in via Eclipse Marketplace

# Configuration Customization

Edit eclipse.ini to include, under `-vmargs`:

```
-Duser.name=(username)
-Xms256m
-Xmx2048m
```

These edits do the following:

- `-Duser.name`
  - Sets the value of the `user` variable in Eclipse templates
- `-Xms256m`
  - Increases the minimum amount of memory allocated for the Java process running Eclipse to 256 MB
- `-Xmx2048m`
  - Increases the maximum allowed memory for the Java process running Eclipse to 2 GB

Finally, setup JDK bindings
