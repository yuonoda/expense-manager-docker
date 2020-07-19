FROM amazonlinux:2

RUN cp /usr/share/zoneinfo/Japan /etc/localtime

WORKDIR /tmp

#### ps command #####
RUN yum -y install procps  \
    && yum clean all

#### nodejs ####
RUN curl -sL https://rpm.nodesource.com/setup_12.x | bash - \
    && yum install -y nodejs \
    && curl -sL https://dl.yarnpkg.com/rpm/yarn.repo | tee /etc/yum.repos.d/yarn.repo \
    && yum install -y yarn \
    && yum install -y libpng libpng-devel \
    && yum clean all


#### set up ####
RUN mkdir -p /var/www/html

WORKDIR /var/www/html
EXPOSE 3000
