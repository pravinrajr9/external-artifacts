#Open Cloud Integrity Technology


**The Open CIT external artifacts project provides :** A couple of external dependencies required to build Open CIT successfully.

# Prerequisites #

To build this project, you will need to download a couple of artifacts and place them in specific directories so we can help you install to your local maven repo.

After you clone the project, cd to the root directory of external artifacts

    cd opencit-external-artifacts

Now download each artifact and prepare them to build the opencit-external-artifacts project.

### Monit ###

    wget https://mmonit.com/monit/dist/monit-5.5.tar.gz
    mv monit-5.5.tar.gz monit/monit-5.5-linux-src.tgz

### Citrix SDK ###

Download the SDK zip file from:

*https://www.citrix.com/downloads/xenserver/product-software/xenserver-6-1.html#ctx-dl-eula*

The zip file is located under 'Development Components>SDK (Software Development Kit)>Download'

**Note:** You need to create an account to download from this site.

You will get the following zip file *'XenServer-6.1-SDK.zip'*, Unzip it and copy the jar file:

    unzip XenServer-6.1-SDK.zip
    mv XenServer-SDK/XenServerJava/bin/xenserver-6.1.0-1.jar citrix-sdk/citrix-sdk-6.1.jar


### Tomcat ###

    wget https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.34/bin/apache-tomcat-7.0.34.tar.gz
    mv apache-tomcat-7.0.34.tar.gz apache-tomcat/apache-tomcat-7.0.34.tar.gz


### Glassfish ###
    wget http://download.java.net/glassfish/4.0/release/glassfish-4.0.zip
    mv glassfish-4.0.zip glassfish/glassfish-4.0.zip
    
### vijava ###
    wget https://sourceforge.net/projects/vijava/files/vijava/VI%20Java%20API%205.5%20Beta/vijava55b20130927.zip
    unzip vijava55b20130927.zip
    mv vijava55b20130927.jar vijava/vijava-5.5.jar


### JDK ###

Download the JDK from:

*http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html#jdk-7u51-oth-JPR*

Download the following file: *jdk-7u51-linux-x64.tar.gz*

Once you downloaded the file, place it in the jdk directory

    mv jdk-7u51-linux-x64.tar.gz jdk/jdk-1.7.0_51-linux-x64.tar.gz

Now cleanup

    rm -rf *.zip
    rm -rf *.jar
    rm -rf XenServer-SDK


# Build #

You are now ready to build, run

    ant


Please see the [How to Build](https://github.com/opencit/opencit/wiki/Open-CIT-2.0.7---How-To-Build) for further details on how this project is used.