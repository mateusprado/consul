consul-server

## Usage example
$ docker run -p 8400:8400 -p 8500:8500 -p 8600:53/udp -h node1 mateusprado/consul-server -data-dir /ui

## DNS test
$ dig @{container_ip} -p 8600 node1.node.consul

## API
$ curl http://{docker_host}/v1/catalog/nodes
[{"Node":"node1","Address":"172.17.0.75"}] ~>
