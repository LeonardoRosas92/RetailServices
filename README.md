# Proyecto microservicios Retail Services 

## Compilacion 
```bashcd
    cd api-manager/
    mvn clean package  

    cd order-service/
    mvn clean package  

    cd user-service/
    mvn clean package  

    cd product-service/
    mvn clean package  
```
Levantar BD
```
    Usuario: postgres
    docker run --name postgresdb -p 5432:5432 -e POSTGRES_DB=unbound -e POSTGRES_PASSWORD=postgres123 -d postgres
```
Actualizar BD
````
cd liquibase
liquibase --changeLogFile="changesets/db.changelog-master.xml" update
````
Levantar servicios  
````
cd api-manager
java -jar target/*.jar

cd order-service/
java -jar order-web/target/*.jar

cd product-service/
java -jar product-web/target/*.jar

cd user-service/
java -jar user-web/target/*.jarjava -jar
````

Verificar instalcaion 
````
http://localhost:8000
````


