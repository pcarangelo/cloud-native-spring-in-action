`.\gradlew test`

`.\gradlew test --tests BookValidationTests`

`.\gradlew bootRun`

`.\gradlew bootJar`

`java -jar build/libs/catalog-service-0.0.1-SNAPSHOT.jar`

`.\gradlew bootBuildImage`

`podman run --rm --name catalog-service -p 8080:8080 catalog-service:0.0.1-SNAPSHOT`

`podman login docker.com`

`podman tag docker.io/library/catalog-service:0.0.1-SNAPSHOT psoftg/catalog-service:0.0.1`

`podman push psoftg/catalog-service:0.0.1`

`kubectl create deployment catalog-service --image=psoftg/catalog-service:0.0.1`

`kubectl expose deployment catalog-service --name=catalog-service --port=8080`

`kubectl port-forward service/catalog-service 8000:8080`

`java -jar build/libs/catalog-service-0.0.1-SNAPSHOT.jar --polar.greeting="Welcome to the catalog from CLI"` override property with cli

`java '-Dpolar.greeting="Welcome to the catalog from JVM"' -jar build/libs/catalog-service-0.0.1-SNAPSHOT.jar` override property with JVM system property

`$env:POLAR_GREETING="Welcome to the catalog from ENV"; java -jar catalog-service-0.0.1-SNAPSHOT.jar` run in powershell, override property with environmento

`podman run -d --name polar-postgres -e POSTGRES_USER=user -e POSTGRES_PASSWORD=password -e POSTGRES_DB=polardb_catalog -p 5432:5432 postgres:14.4`

Chapter 5 complete