FROM centos
# author: frank_lin@whu.edu.cn

# running required command
RUN yum -y update
RUN yum install vim -y
RUN yum install java-1.8.0-openjdk.x86_64 -y
RUN yum install git -y

WORKDIR /
# copy the code
# COPY lanproxy-client /lanproxy-client
RUN git clone https://github.com/massinger/lanproxy-client.git

ENTRYPOINT ["/lanproxy-client/init.sh"]
WORKDIR /lanproxy-client
# EXPOSE 8888
CMD ["/bin/bash"]
