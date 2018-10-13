# Postgres Docker
This is an unofficial, open-source for POSTGRES based projects that run on Docker-Compose. 

    Postgres 9.3
    
## Usage
You are up and running in three simple steps:

$ cd docker-postgres

$ docker-compose up --build -d 
  
## Backup / Restore

  sudo docker exec -i postgres pg_dump -U postgres -d database > postgres/db/dumps/dump_`date +%d-%m-%Y"_"%H_%M_%S`.sql

* Restore from a backup 

  See the list of backups, you can run:

  sudo docker exec postgres ls /db/dumps

* Restore

  sudo docker exec -i postgres psql -U postgres -d database < postgres/db/dumps/dump.sql
