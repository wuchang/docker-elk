# https://github.com/elastic/elasticsearch-docker
#FROM docker.elastic.co/elasticsearch/elasticsearch:5.3.0
FROM elasticsearch:5.4.0



# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
RUN mkdir /usr/share/elasticsearch/plugins/ik \
    && wget https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v5.4.0/elasticsearch-analysis-ik-5.4.0.zip -O /tmp/ik.zip \
    && unzip -o /tmp/ik.zip -d /usr/share/elasticsearch/plugins/ik \
    && rm /tmp/ik.zip \
    && bin/elasticsearch-plugin install analysis-smartcn \
    && bin/elasticsearch-plugin install analysis-icu  
RUN bin/elasticsearch-plugin install x-pack

