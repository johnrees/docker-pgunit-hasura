1. (install docker, then) `docker-compose up --build -d`

2. (install hasura CLI, then) `hasura console`

3. open http://localhost:8002. `test` table should exist, make some changes e.g. add a new table. Some files should now be updated in /metadata and /migrations
