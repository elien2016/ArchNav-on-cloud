# ArchNav-on-cloud

Dockerfiles and Docker run commands to migrate the ArchNav application to the cloud

## ApacheDS

`docker run -d –name ads -p 10389:10389 itzg/apacheds`

## Tomcat

```
docker run -d –name tomcat -p 8080:8080 elien2016/tomcat sleep infinity
docker exec -it tomcat sh
# cd bin
# cat catalina.sh | sed ‘s/\r$//’ > catalina2.sh
# catalina2.sh run
```

## GlassFish

```
docker run -d –name glassfish -p 4848:4848 -p 8080:8080 elien2016/glassfish sleep infinity
docker exec -it tomcat sh
# cd bin
# asadmin enable-secure-admin
# asadmin start-domain domain1
```
