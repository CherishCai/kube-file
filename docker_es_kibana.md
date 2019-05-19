
docker run -d --restart=unless-stopped -p 9200:9200 -p 9300:9300 -p 5601:5601 -v /root/.data/es_data:/usr/share/elasticsearch/data --ulimit nofile=65536:65536 -e "bootstrap.memory_lock=true" --ulimit memlock=-1:-1 -e "discovery.type=single-node" --name elasticsearch docker.elastic.co/elasticsearch/elasticsearch:6.2.4

docker run -d -e ELASTICSEARCH_URL=http://127.0.0.1:9200 --name kibana --network=container:elasticsearch docker.elastic.co/kibana/kibana:6.2.4


docker run -d --restart=unless-stopped -p 9200:9200 -p 9300:9300 -v /root/.data/es_data:/usr/share/elasticsearch/data --ulimit nofile=65536:65536 -e "bootstrap.memory_lock=true" --ulimit memlock=-1:-1 -e "discovery.type=single-node" --name elasticsearch docker.elastic.co/elasticsearch/elasticsearch:6.2.4

docker run -d -e ELASTICSEARCH_URL=http://172.17.0.2:9200 --name kibana docker.elastic.co/kibana/kibana:6.2.4


