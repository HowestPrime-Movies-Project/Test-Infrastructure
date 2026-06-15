

### Start the test environment:
`docker compose -f howestprime-test/docker-compose.yml up -d --remove-orphans`

### Shut down the test environment:
`docker compose -f howestprime-test/docker-compose.yml  down &`

### Check the logs of a specific container:
`docker logs -f <container_name>`

### QUICK LINKS
> [Client WebApp](http://localhost:10200/)

> [Client Backoffice](http://localhost:10210/)

> [Movies API Swagger](http://localhost:40220/swagger)

> [Ticketing API Swagger](http://localhost:40230/swagger)

> [LavinMQ Management UI](http://localhost:40201/)
