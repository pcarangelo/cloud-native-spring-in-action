`.\gradlew test`

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

` kubectl port-forward service/catalog-service 8000:8080`