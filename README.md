mvn clean install -DskipTests=true
### To run postgres & pgadmin in container
```
docker-compose up -d
docker-compose down
```
Access pgadmin
```
http://localhost:5050/
```
Register new server
```
General > Name: anyname 
Connection > hostname: postgresqldb
username: root
password: root
Save
```

### Test
Return list of all the products loaded into db on startup.
```
http://localhost:8080/products
```

### Issues
to refresh the sbprogres image
```
mvn clean install -DskipTests=true
docker-compose build --no-cache
```
