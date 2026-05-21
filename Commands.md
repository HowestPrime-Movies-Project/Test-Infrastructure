Build Movie Microservice image
`dotnet publish src/Howestprime.Movies.Main/ --os linux /t:PublishContainer /p:PublishProfile=test /p:ContainerImageName=howestprime-movies-api`

Build client backoffice image
`dotnet publish Howestprime.Backoffice/ --os linux /t:PublishContainer /p:PublishProfile=test /p:ContainerImageName=howestprime-backoffice`

Build Ticketing Microservice image
`docker build -t ticketing-service -f Dockerfile ../st-microservice-ticketing-Maurice-De-Kegel/`
