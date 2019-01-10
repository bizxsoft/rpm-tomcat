rpm-tomcat
===========

An RPM spec file to install Tomcat 8.X.

To Build:

git clone https://github.com/bizxsoft/rpm-tomcat.git && cd rpm-tomcat

yum -y install rpmdevtools

./make_rpm.sh

yum install -y redhat-lsb-core

rpm -ivh rpmbuild/RPMS/noarch/tomcat-8.5.9-1.noarch.rpm
