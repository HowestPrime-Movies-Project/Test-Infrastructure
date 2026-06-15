# Build commands

Run these from the root of each respective repository.

### Build Movies Microservice image
Run from `st-microservice-movies-Maurice-De-Kegel/`:
```
dotnet publish src/Howestprime.Movies.Main/ --os linux /t:PublishContainer /p:PublishProfile=test /p:ContainerImageName=howestprime-movies-api
```

### Build Client Backoffice image
Run from `st-client-backoffice-Maurice-De-Kegel/`:
```
dotnet publish Howestprime.Backoffice/ --os linux /t:PublishContainer /p:PublishProfile=test /p:ContainerImageName=howestprime-backoffice
```

### Build Ticketing Microservice image
Run from `st-infrastructure-test-Maurice-De-Kegel/`:
```
docker build -t ticketing-service -f Dockerfile ../st-microservice-ticketing-Maurice-De-Kegel/
```
