

./logstash agent -v  -f /logsymonitoreo/logstash/data/datacovid.conf



## data covid
PUT /ejemplo8
{
  "mappings": {
    "properties": {
     "rut": {"type":"text"},
     "nombre": {"type":"text"},
     "apellido": {"type":"text"},
     "edad": {"type":"integer"},
     "fecha-contagio": {"type":"text"},
     "sintomas": {"type":"boolean"},
     "nivel": {"type":"integer"},
     "ciudad": {"type":"text"}
    }
  }
}


# 

PUT /usuarios

{

  "mappings": {

    "properties": {

      "nombre" : {"type": "text"},

      "apellido" : {"type": "text"},

      "edad" : {"type": "integer"},

      "visitas" : {"type": "integer"},

      "preferencial" : {"type": "text"},

      "preferencial2" : {"type": "text"}

    }

  }

  

}






docker pull docker.elastic.co/logstash/logstash:7.12.0


docker run --rm -it -v /Users/dbell/Dropbox/Diplomadousach/logsymonitoreo/logstash/data:/usr/share/logstash/pipeline/ docker.elastic.co/logstash/logstash:7.12.0 -f /usr/share/logstash/pipeline/datacovid.conf


docker run  --link elasticsearch:elasticsearch --rm -it  docker.elastic.co/logstash/logstash:7.12.0
