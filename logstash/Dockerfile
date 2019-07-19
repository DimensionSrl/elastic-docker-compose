# https://github.com/elastic/logstash-docker
FROM docker.elastic.co/logstash/logstash:7.2.0

# Add your logstash plugins setup here
# Example: RUN logstash-plugin install logstash-filter-json

RUN logstash-plugin install logstash-input-http
RUN logstash-plugin install logstash-input-http_poller
RUN logstash-plugin install logstash-input-imap
# # I know, we should use a Gemfile
# RUN /usr/share/logstash/bin/ruby -S gem install redis belzebuth benchmark-ips ci_reporter rspec-support rspec-core diff-lcs rspec-expectations rspec-mocks rspec ci_reporter_rspec safe_yaml crack fivemat flores gem_publisher json-schema rspec-wait logstash-devutils rack-test hashdiff
# RUN /usr/share/logstash/bin/ruby -S gem install webmock -v 3.5.1
# RUN /usr/share/logstash/bin/ruby -S gem install hashdiff -v 0.3.9
# RUN /usr/share/logstash/bin/ruby -S gem install kramdown -v 1.14.0