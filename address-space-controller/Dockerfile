FROM enmasseproject/java-base:8-7

RUN yum -y install openssl && yum -y clean all

ARG version=latest
ENV VERSION ${version}
ADD target/address-space-controller-${VERSION}.jar /address-space-controller.jar
ENV LOG_LEVEL info

CMD ["/opt/run-java/launch_java.sh", "/address-space-controller.jar"]
