## Development
#### To build dockerfile
Change directory to location of Dockerfile or point the following command to the directory containing the Dockerfile
```
docker build .
```

#### Tag the image
Take the image ID created for the image when the build is successful 
Use a tag name that includes your username so can push to your docker hub repository
```
docker tag <image ID> <tag name>
```

#### Push the image 
```
docker login
```
Enter login details

```
docker push <tag name>
```


## To Run
```
docker run -p 8888:8888 moocarme/pydata1.0
```


## Setting up on an EC2 instance

- Start an ec2 instance
- Update and install docker
```
sudo yum update -y
sudo yum install -y docker
```

- Start docker daemon
```
sudo service docker start
```

- Run image
```
sudo docker run -p 8888:8888 moocarme/pydata1.0
```
