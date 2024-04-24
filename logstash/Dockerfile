ARG ELASTIC_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:${ELASTIC_VERSION}

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json
USER root

RUN apt install -y shared-mime-info
RUN ruby -S gem install mimemagic -v '>= 0.4.3'
RUN logstash-plugin install logstash-input-google_cloud_storage
