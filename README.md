# docker-registry-s3
docker-registry-s3

Place the AWS Credentials value 

```
<AWS Region>
```

```
<AWS Access Key>
```

```
<AWS Secret Key>
```
```
<AWS S3 bucket nmae>
```

## Set up for docker registry ##


```
docker run --entrypoint htpasswd registry:2 -Bbn admin admin@123 > auth/htpasswd
```

```
docker-compose up --build -d
```

Test docker registry 

```
docker login localhost:9099
user: 
password:
```

```
docker pull busybox
docker tag busybox localhost:9099/busybox
docker push localhost:9099/busybox
```