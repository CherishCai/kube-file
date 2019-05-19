--restart=unless-stopped

docker run -d -p 5601:5601 -it -e ELASTICSEARCH_URL=http://122.152.219.238:9200 --name kibana docker.elastic.co/kibana/kibana:6.2.4
