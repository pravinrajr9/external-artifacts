#Open Cloud Integrity Technology


**The Open CIT external artifacts project provides :** A couple of external dependencies required to build Open CIT successfully.

# Prerequisites #

To build this project, you will need to download a couple of artifacts and place them in specific directories so we can help you install to your local maven repo.

After you clone the project, cd to the root directory of external artifacts

    cd opencit-external-artifacts
	git checkout release-cit-2.2

Now download each artifact and prepare them to build the opencit-external-artifacts project.


### Apache Tomcat ###

    wget https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.34/bin/apache-tomcat-7.0.34.tar.gz
    mv apache-tomcat-7.0.34.tar.gz apache-tomcat/apache-tomcat-7.0.34.tar.gz


## JRE Windows ###

Download the JRE Windows from:

*http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html*

Download the following file: *jre-8u121-windows-x64.tar.gz*

Once you download the file, place it in the jre-windows directory

    mv jre-8u121-windows-x64.tar.gz jre-windows/jre-1.8-windows-x64.tar.gz


### Monit ###

    wget https://mmonit.com/monit/dist/monit-5.5.tar.gz
    mv monit-5.5.tar.gz monit/monit-5.5-linux-src.tgz


### kmip4j ###
    wget https://sourceforge.net/projects/kmip4j/files/KMIP4J-V1.0/kmip4j-bin-1.0.zip
    unzip kmip4j-bin-1.0.zip
    mv jar/kmip4j.jar kmip4j/kmip4j-1.0.jar

### TPM Tools ###
    wget https://sourceforge.net/projects/trousers/files/tpm-tools/1.3.8/tpm-tools-1.3.8.tar.gz/download
    mv tpm-tools-1.3.8.tar.gz tpm-tools/tpm-tools-1.3.8.tar.gz


### vijava ###
    wget https://sourceforge.net/projects/vijava/files/vijava/VI%20Java%20API%205.5%20Beta/vijava55b20130927.zip
    unzip vijava55b20130927.zip
    mv vijava55b20130927.jar vijava/vijava-5.5.jar

### ext2fsd ###
    wget --no-check-certificate  https://sourceforge.net/projects/ext2fsd/files/Ext2fsd/0.62/Ext2Fsd-0.62.exe
    mv Ext2Fsd-0.62.exe ext2fsd/Ext2Fsd-0.62.exe


Now cleanup

    rm -rf *.zip
    rm -rf *.jar
    rm -rf *.exe
    rm -rf XenServer-SDK


# Build #

You are now ready to build, run

    ant


Please see the [Product Guide](https://github.com/opencit/opencit/wiki/Open-CIT-2.2-Product-Guide) for further details on how this project is used.