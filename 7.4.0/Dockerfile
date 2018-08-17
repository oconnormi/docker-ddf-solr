FROM alpine as prep

ENV JTS_VERSION=1.15.0
ENV SOLR_XPATH_VERSION=2.14.0-SNAPSHOT
ENV SOLR_XPATH_REPO=snapshots

RUN apk add --no-cache curl
RUN mkdir /deps
RUN curl -Ls "https://search.maven.org/remotecontent?filepath=com/vividsolutions/jts/$JTS_VERSION/jts-$JTS_VERSION.jar" -o "/deps/jts-$JTS_VERSION.jar"
RUN curl -Ls "http://artifacts.codice.org/service/local/artifact/maven/content?r=$SOLR_XPATH_REPO&g=ddf.platform.solr&a=solr-xpath&v=$SOLR_XPATH_VERSION" -o "/deps/solr-xpath-$SOLR_XPATH_VERSION.jar"

FROM solr:7.4.0

COPY --from=prep /deps/*.jar /opt/solr/server/solr-webapp/webapp/WEB_INF/lib/
