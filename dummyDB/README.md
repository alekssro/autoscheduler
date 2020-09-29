# Create MongoDB Data Base

The Data Base container can be built and run from a backup file by following the next commands:

## 1. Run mongodb container with name autoschedule-database
```{bash}
docker run --name autoschedule-database -d -p 27017:27017 mongo:latest
```

## 2. Copy backup info to container
```{bash}
docker cp ./dummyDB/backup/ autoschedule-database:/backup/
```

## 3. Restore backup
```{bash}
docker exec autoschedule-database mongorestore -h localhost:27017 /backup/
```