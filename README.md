# Structure du projet

docker-mysql-lab/
├── Dockerfile
├── .env
├── init.sql
├── README.md


# Les étapes de build / run

docker build -t mysql-lab .
docker run --name mysql-lab-container -d --env-file .env mysql-lab

# Vérifications

docker exec -it mysql-lab-container bash
mysql -u root -p
SHOW DATABASES;
USE formation;
SHOW TABLES;
SELECT * FROM utilisateurs;


