FROM ubuntu:focal 

# => Stage 1: System prereqs
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive \
    TZ=etc/UTC \
    apt-get install -y \
      build-essential \
      ruby \
      ruby-dev \
      gem 

# => Stage 2: Install the plugin
RUN gem install fluentd --no-doc && \
    gem install fluent-plugin-out-solr

# => Run stage
ENTRYPOINT exec fluentd -c /fluentd/fluentd.conf -v
