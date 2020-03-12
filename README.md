# Elasticsearch

Cluster Formation

Creating 3 node cluster

For Node 1 (Master node)

•	cluster.name: cluster-1 <br />
•	node.name: master-1 <br />
•	node.master: true <br />
•	node.data: false <br />
•	node.ingest: false <br />
•	node.ml: false <br />
•	network.host: 192.168.43.90 <br />
•	http.port: 9201 <br />
•	transport.host: localhost <br />
•	transport.tcp.port: 9301 <br />
•	cluster.initial_master_nodes: [“master-1”] <br />
•	discovery.zen.ping.unicast.hosts: [“192.168.43.90:9201”] <br />


For Node 2 (Data node)

•	cluster.name: cluster-1 <br />
•	node.name: data-1 <br />
•	node.master: false <br />
•	node.data: true <br />
•	node.ingest: false <br />
•	node.ml: false <br />
•	network.host: 192.168.43.90 <br />
•	http.port: 9202 <br />
•	transport.host: localhost <br />
•	transport.tcp.port: 9302 <br />
•	discovery.seed_hosts: [“localhost:9301”] <br /> 


For Node 3 (Coordinating node)

•	cluster.name: cluster-1 <br />
•	node.name: coord-1 <br />
•	node.master: false <br />
•	node.data: false <br />
•	node.ingest: false <br />
•	node.ml: false <br />
•	network.host: 192.168.43.90 <br />
•	http.port: 9203 <br />
•	transport.host: localhost <br />
•	transport.tcp.port: 9303 <br />
•	discovery.seed_hosts: [“localhost:9301”,”localhost:9302”] <br /> 
