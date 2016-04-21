# Jetbrains Upsource
Docker image: Alpine Linux 3.3- openJAVA JRE 8- Jetrbains Upsource 3.0


##Usage

Pull the image, create a new container with your data in volumes and start it:

```bash
docker pull boutch/jetbrains-upsource
docker create --name jetbrains-upsource -p 8080:8080 --restart=always boutch/jetbrains-upsource
docker start jetbrains-upsource
```

Mount your data in volume:

```bash
docker run -dit --name jetbrains-upsource -p 8080:8080 \
    -v /srv/jetbrains-upsource:/var/lib/upsource -restart=always \
    boutch/jetbrains-upsource
```


