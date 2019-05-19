
docker run -d --restart=unless-stopped -p 5601:5601 -it -e ELASTICSEARCH_URL=http://127.0.0.1:9200 docker.elastic.co/kibana/kibana:6.2.4
