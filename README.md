# INSTALL CASAOS ON DOCKER CONTAINER
no need to install casaos on bare-metal. crated for mobility
run:
```
docker-compose up -d
```
```http://localhost:8085```

## (optional) set casaos docker to systemd for automatic restart when computer shutdown

edit file casaos.service
```
nano casaos.service
# Pastikan environment-nya cocok
User=user #sesuaikan
Group=user #sesuaikan
```

```
sudo cp casaos.service /etc/systemd/system/casaos.service
sudo systemctl daemon-reload
sudo systemctl enable casaos.service
sudo systemctl start casaos.service
```