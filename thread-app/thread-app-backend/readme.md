<!-- docker compose -->

version: '3.4'

services:
  postgres:
    container_name: threads-db
    image: postgres
    ports:
      - 5432:5432
    volumes:
      - postgres_data:/var/lib/postgresql/data
    environment:
      POSTGRES_USER: postgres
      POSTGRES_DB: threads
      POSTGRES_PASSWORD: threads

volumes:
  postgres_data:

# docker compose up // To run the docker-compose.yml file
# docker compose up -d // To run the docker-compose.yml file in background

# npx prisma init // To initialize the prisma

# docker ps // to list container
# docker exec -it container_id bash // To enter in container

# su user_name // To enter in postgres with user
# psql // To enter in command line db
# \l // to list all database
# \c database_name // to access database

# npx prisma migrate dev --name create_users_table // To do prisma migration with migration name "create_users_table"
