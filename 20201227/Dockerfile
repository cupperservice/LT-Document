FROM centos:7

RUN yum update -y && \
yum install -y curl && \
yum install -y unzip && \
yum install -y zip && \
yum install -y which && \
curl -s "https://get.sdkman.io" | bash && \
source "/root/.sdkman/bin/sdkman-init.sh"

CMD tail -f > /dev/null
