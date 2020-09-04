FROM ruby:2.7-buster

# => Install fluentd + solr plugin
RUN gem install fluentd --no-doc && \
    gem install fluent-plugin-out-solr

# => Run stage
ENTRYPOINT exec fluentd -c /fluentd/fluentd.conf -v
