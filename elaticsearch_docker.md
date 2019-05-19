
docker run -d --restart=unless-stopped -p 9200:9200 -p 9300:9300 -v /root/.data/es_data:/usr/share/elasticsearch/data --ulimit nofile=65536:65536 -e "bootstrap.memory_lock=true" --ulimit memlock=-1:-1 -e "discovery.type=single-node" --name elasticsearch docker.elastic.co/elasticsearch/elasticsearch:6.2.4
