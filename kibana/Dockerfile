# https://github.com/elastic/kibana-docker
FROM docker.elastic.co/kibana/kibana:7.3.1


USER root
# Add your kibana plugins setup here
# Example: RUN kibana-plugin install <name|url>
RUN yum install -y git gcc-c++ make
RUN curl -sL https://rpm.nodesource.com/setup_10.x | bash -
RUN yum install -y nodejs
RUN npm install -g bower
WORKDIR "/opt/kibana/plugins"
RUN git clone https://github.com/nreese/kibana-time-plugin.git
WORKDIR "/opt/kibana/plugins/kibana-time-plugin"
RUN sed -i -e 's/"version".*/"version" : "7.3.1"/' package.json
RUN bower install --allow-root
WORKDIR "/opt/kibana"



#WORKDIR "/opt/kibana/plugins"
#RUN git clone https://github.com/virusu/3D_kibana_charts_vis.git 3D_kibana_charts_vis
#WORKDIR  "/opt/kibana/plugins/3D_kibana_charts_vis"
#RUN sed -i -e 's/"version".*/"version" : "7.3.1"/' package.json
#RUN npm install
#
#WORKDIR "/opt/kibana"


CMD ["/usr/local/bin/kibana-docker","--allow-root"]


