FROM ubuntu:14.04
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

RUN apt-get install -y curl
RUN echo "deb [arch=amd64] http://archive.cloudera.com/cdh5/ubuntu/precise/amd64/cdh precise-cdh5 contrib" | tee -a /etc/apt/sources.list.d/cloudera.list
RUN echo "deb-src http://archive.cloudera.com/cdh5/ubuntu/precise/amd64/cdh precise-cdh5 contrib" | tee -a /etc/apt/sources.list.d/cloudera.list
RUN curl -s http://archive.cloudera.com/cdh5/ubuntu/precise/amd64/cdh/archive.key | sudo apt-key add -
RUN sudo apt-get update
RUN apt-get install -y openjdk-7-jdk
RUN apt-get install -y build-essential lsof 
RUN touch /etc/apt/preferences.d/cloudera.pref
RUN echo "Package: *" | tee -a /etc/apt/preferences.d/cloudera.pref
RUN echo "Pin: release o=Cloudera, l=Cloudera" | tee -a /etc/apt/preferences.d/cloudera.pref
RUN echo "Pin-Priority: 501" | tee -a /etc/apt/preferences.d/cloudera.pref
RUN apt-get install -y zookeeper-server
RUN service zookeeper-server init

#CMD ["/etc/init.d/zookeeper-server start"]

EXPOSE      2181
#ENTRYPOINT  ["/usr/bin/redis-server"]


#sudo docker build -t davidmontgom/zookeeper .
#sudo docker run --name zk1 -d -i -t davidmontgom/zookeeper   #Run in background remove d to run ih foreground
#sudo docker run --name kafka  -d -P davidmontgom/zookeeper  
#sudo docker run --name kafka  -d -p 6379:6379 davidmontgom/zookeeper  
#sudo docker run -d -p 127.0.0.1:2181:2181 davidmontgom/zookeeper 
#sudo docker attach 665b4a1e17b6 #by ID
#sudo docker exec -it <CONTAINER ID> /bin/bash

#docker rm $(docker ps -aq) remove all contaners

#sudo docker push davidmontgom/redis
#remove from remote sudo docker rmi training/sinatra





-d, --detach=false         Detached mode: run the container in the background and print the new container ID
-i, --interactive=false    Keep STDIN open even if not attached
-t, --tty=false            Allocate a pseudo-TTY







