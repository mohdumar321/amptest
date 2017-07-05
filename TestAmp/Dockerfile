FROM centos:7

RUN yum update -y && \
yum install -y wget && \
yum install -y java-1.8.0-openjdk java-1.8.0-openjdk-devel && \
yum clean all

RUN wget http://download.cloudsoft.io/amp/4.6.0-atos/cloudsoft-amp-karaf-4.6.0-atos-noarch.rpm 
RUN yum -y install cloudsoft-amp-karaf-4.0.0-atos-noarch.rpm

RUN initctl start amp

# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["bash"]
