## Moebius redis
> At first, follow the below common steps to install on **aws ami**.

```shell script
sudo su -

yum install docker
yum install git
curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

service docker start
git clone https://github.com/team-moebius/redis.git
```

### Master server
```shell script
../master$ docker-compose up -d
```
### Slave server
```shell script
../slave$ docker-compose up -d
```