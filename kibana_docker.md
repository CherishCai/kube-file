--restart=unless-stopped

docker run -d -p 5601:5601 -it -e ELASTICSEARCH_URL=http://127.0.0.1:9200 --name kibana --network=container:elasticsearch docker.elastic.co/kibana/kibana:6.2.4
