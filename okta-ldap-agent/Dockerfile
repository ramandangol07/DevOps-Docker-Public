FROM centos:7
MAINTAINER Alex Franks <alex-envoy@users.noreply.github.com>

RUN yum update -y && \
    yum install -y https://weareenvoy-admin.okta.com/static/ldap-agent/OktaLDAPAgent-05.06.05.x86_64.rpm && \
    yum clean all

RUN mv /opt/Okta/OktaLDAPAgent/conf/logback.xml /opt/Okta/OktaLDAPAgent/logback-default.xml

ADD start.sh /start.sh

VOLUME ["/opt/Okta/OktaLDAPAgent/conf"]

CMD ["/start.sh"]
