# Taller Kubernetes

kubectl apply -f namespace.yaml

## ConfiMaps y Secrets
#### desde la carpeta yaml

kubectl apply -f ./database/mongo-config.yaml -f ./database/mongo-secret.yaml -f ./database/mongo.yaml -f ./database/mysql-config.yaml -f ./database/mysql-secret.yaml -f ./database/mysql.yaml

## Interfaces para las Bases de Datos

kubectl apply -f ./database/mongo-express.yaml -f ./database/phpmyadmin.yaml

## Backend

kubectl apply -f ./backend/reviews.yaml -f ./backend/catalog.yaml -f ./backend/store.yaml

## Frontend

kubectl apply -f ./frontend/fe-config.yaml -f ./frontend/fe-reviews.yaml -f ./frontend/fe-catalog.yaml -f ./fe-frontend/store.yaml

## Monitoreo

kubectl get all -n backends -o wide
kubectl get all -n databases -o wide
kubectl get all -n frontends -o wide