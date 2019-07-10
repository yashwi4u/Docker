#FROM ubuntu
RUN apt-get update

#Making the Work Directory
RUN mkdir /myfiles
WORKDIR /myfiles
COPY . /myfiles/

#Installing python and other essentials
RUN apt-get install -y software-properties-common
RUN apt-get install -y nano
RUN apt-get install -y build-essential python3-dev python3-pip

#Installing JAVA
RUN apt install -y openjdk-8-jdk
RUN echo "JAVA_HOME="/usr/lib/jvm/java-8-openjdk-amd64/jre/"">>/etc/environement
ENV JAVA_HOME="/usr/lib/jvm/jdk1.8.0_211"

#Installing Spark
RUN mv spark_installer /usr/local/spark
ENV SPARK_HOME="/usr/local/spark"
ENV PATH="$PATH:/usr/local/spark/bin"

#Installing contents in requirements.txt
RUN apt-get install -y unixodbc-dev
RUN pip3 install -r requirements.txt

#Mysql part
RUN apt-get install -y mysql-server mysql-common mysql-client

#Installing Nginx
RUN apt-get install -y nginx

ENV PYTHONUNBUFFERED 1
