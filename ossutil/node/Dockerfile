FROM node:10.17.0-stretch-slim

ARG OSSUTIL_VERSION=1.6.10
ADD http://gosspublic.alicdn.com/ossutil/${OSSUTIL_VERSION}/ossutil64 /usr/bin/
RUN chmod a+x /usr/bin/ossutil64 && \
    ln -s /usr/bin/ossutil64 /usr/bin/ossutil

ENV OSS_ENDPOINT=''
ENV OSS_AK_ID=''
ENV OSS_AK_SECRET=''
ENV OSSUTIL_CONFIG_FILE=''

COPY docker-entrypoint.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/docker-entrypoint.sh
ENTRYPOINT [ "docker-entrypoint.sh" ]
