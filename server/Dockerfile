FROM mateusprado/consul:latest

ADD ./config /config/

ADD https://dl.bintray.com/mitchellh/consul/0.5.2_web_ui.zip /tmp/webui.zip

RUN cd /tmp && unzip webui.zip && mv dist /ui && rm webui.zip

EXPOSE 8300 8301 8301/udp 8302 8302/udp 8400 8500 53/udp

ENTRYPOINT ["/bin/consul", "agent", "-server", "-config-dir=/config"]
