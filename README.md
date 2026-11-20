# Laboratorio de prueba de HDFS, MapReduce/YARN y prueba de fallos

Este proyecto sirve para probar las funciones principales de Hadoop, como la division de bloques, prueba de caida de nodos y ejecución de MapReduce sobre un texto de prueba

## Ejecución

Para ejecutar el proyecto deberá tener docker instalado y ejecutar el docker-compose dentro del fichero docker

"docker compose up -d"

Dentro de bash podra realizar las pruebas de la actividad

"docker exec -it namenode bash"

## Nota tecnica

En la prueba de MapReduce se ha tenido que aumentar el espacio de memoria debido a que el proceso tardaba en empezar más de la cuenta.
 
Se ha modificado el config con las siguientes lineas:

"MAPRED-SITE.XML_yarn.app.mapreduce.am.resource.mb=1024
MAPRED-SITE.XML_mapreduce.map.memory.mb=1024
MAPRED-SITE.XML_mapreduce.reduce.memory.mb=1024
MAPRED-SITE.XML_yarn.app.mapreduce.am.command-opts=-Xmx768m
MAPRED-SITE.XML_mapreduce.map.java.opts=-Xmx768m
MAPRED-SITE.XML_mapreduce.reduce.java.opts=-Xmx768m"
