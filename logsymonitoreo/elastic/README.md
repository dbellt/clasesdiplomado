##
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.12.0
docker network create elastic
docker run -d  --name elasticsearch --net elastic -p 9200:9200 -p 9300:9300 -it -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.12.0
