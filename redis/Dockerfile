FROM        ubuntu:14.04
RUN         apt-get update && apt-get install -y redis-server
EXPOSE      6379
ENTRYPOINT  ["/usr/bin/redis-server"]


#sudo docker build -t davidmontgom/redis .
#sudo docker run --name redis -d davidmontgom/redis
#sudo docker run --name redis -d -P davidmontgom/redis
#sudo docker run --name redis -d -p 6379:6379 davidmontgom/redis
#sudo docker run -d -p 127.0.0.1:6379:6379 davidmontgom/redis

#sudo docker push davidmontgom/redis
#remove from remote sudo docker rmi training/sinatra