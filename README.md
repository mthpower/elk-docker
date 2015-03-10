ELK-Docker
==========

Docker configuration of Elasticsearch, Logstash and Kibana.

Build
=====

In order to build the image:

```
docker build -t elk:latest .
```

Run
===

In order to run the image:

```
docker run -p 5000:5601 -p 1555:1555 --name elk elk
```

This will export to your local port 5000 kibana, so you will be able to access to kibana by:

```
http://localhost:5000
```

Logs can be added by piping them over TCP on port 1555. For python, try python-logstash

TODO
----

- [ ]  I think we don't need to install all this Java things on the image (just openjdk-7-jre-headless).
- [ ]  Push image to docker registry.
- [ ]  Split in three Docker images and use fig to set it up.
