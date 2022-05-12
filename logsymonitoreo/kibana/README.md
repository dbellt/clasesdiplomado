

docker pull docker.elastic.co/kibana/kibana:7.12.0

docker run -d   --name kib-01 --net elastic  -p 5601:5601 -e "ELASTICSEARCH_HOSTS=http://elasticsearch:9200" docker.elastic.co/kibana/kibana:7.12.0
