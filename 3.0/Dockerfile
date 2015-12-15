FROM centos:latest

RUN yum -y update
RUN yum -y install yum-plugin-priorities yum-plugin-fastestmirror
RUN yum -y install vim tar sshd

EXPOSE 22

#ENV CASSANDRA_VERSION 3.0.1

#RUN apt-get update \
#	&& apt-get install -y cassandra="$CASSANDRA_VERSION" \
#	&& rm -rf /var/lib/apt/lists/*

#ENV CASSANDRA_CONFIG /etc/cassandra

#COPY docker-entrypoint.sh /docker-entrypoint.sh
#ENTRYPOINT ["/docker-entrypoint.sh"]

#VOLUME /var/lib/cassandra

# 7000: intra-node communication
# 7001: TLS intra-node communication
# 7199: JMX
# 9042: CQL
# 9160: thrift service
EXPOSE 22 7000 7001 7199 9042 9160
#CMD ["cassandra", "-f"]
