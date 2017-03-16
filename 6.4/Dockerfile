FROM solr:6.4.1

RUN curl -Ls 'http://artifacts.codice.org/service/local/repositories/releases/content/org/codice/thirdparty/jts/1.13/jts-1.13.jar' -o '/opt/solr/server/solr-webapp/webapp/WEB-INF/lib/jts-1.13.jar' \
    && curl -Ls "http://artifacts.codice.org/service/local/artifact/maven/content?r=snapshots&g=ddf.platform.solr&a=solr-xpath&v=2.11.0-SNAPSHOT" -o '/opt/solr/server/solr-webapp/webapp/WEB-INF/lib/solr-xpath-2.11.0-SNAPSHOT.jar'
