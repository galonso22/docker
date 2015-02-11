FROM davidgaya/apache-php-oci:latest

MAINTAINER Gabriel Alonso <gabriel.alonso@intraway.com>

#update and install stuff
RUN apt-get update
RUN apt-get -y install git vim wget build-essential
RUN apt-get -y install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev

#Allow overrida
RUN sed -i 's/AllowOverride None/AllowOverride All/g' /etc/apache2/apache2.conf
RUN a2enmod rewrite

#Add virtual host
ADD iwaycam.localhost.conf /etc/apache2/sites-available/iwaycam.localhost.conf
RUN a2ensite iwaycam.localhost.conf

#Install python
RUN wget http://python.org/ftp/python/2.7.5/Python-2.7.5.tgz
RUN tar -xvf Python-2.7.5.tgz
RUN cd Python-2.7.5 && ./configure && make && sudo make install

#Install Node
RUN wget http://nodejs.org/dist/v0.10.30/node-v0.10.30.tar.gz
RUN tar xfvz node-v0.10.30.tar.gz
RUN cd node-v0.10.30 && ./configure && make && sudo make install

#Install uglify
RUN sudo npm install -g uglify-js
RUN sudo npm install -g uglifycss