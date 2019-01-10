rpm-tomcat
===========

An RPM spec file to install Tomcat 8.X.

To Build:

`sudo yum -y install rpmdevtools`

`rpmdev-setuptree`

`wget http://archive.apache.org/dist/tomcat/tomcat-8/v8.5.9/bin/apache-tomcat-8.5.9.tar.gz -O ~/rpmbuild/SOURCES/apache-tomcat-8.5.9.tar.gz`

`./prepare.bash apache-tomcat-8.5.9.tar.gz`

`rpmbuild -bb ~/rpmbuild/SPECS/tomcat.spec`

To clean the RPM build dir

`rpmdev-wipetree && rm -rf rpmbuild` 

All in one line to rebuild & install the package:

`sudo rpm -e tomcat && rpmdev-wipetree && rm -rf rpmbuild && rpmdev-setuptree && ./prepare.bash apache-tomcat-8.5.9.tar.gz && rpmbuild -bb rpmbuild/SPECS/tomcat.spec && sudo yum install -y rpmbuild/RPMS/noarch/apache-tomcat-8.5.9.noarch.rpm`
