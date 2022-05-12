##

docker pull docker.elastic.co/elasticsearch/elasticsearch:7.12.0

docker run -d -p 9200:9200 -p 9300:9300 --name elasticsearch -e "discovery.type=single-node"  -v /elastic/data:/usr/share/elasticsearch/data docker.elastic.co/elasticsearch/elasticsearch:7.12.0
