FROM nginx:latest

LABEL maintainer="andrew.brown5717@gmail.com"

RUN apt-get update -y && apt-get upgrade -y && apt-get autoclean -y && apt-get autoclean -y
RUN apt-get install -y vim build-essential wget curl git zip unzip

ADD ./scripts/install_nvm.sh /tmp
ADD ./scripts/install_node.sh /tmp

RUN git config --global user.email "andrew.brown5717@gmail.com"
RUN git config --global user.name "Andrew Brown"

RUN touch ~/.bashrc && chmod 766 ~/.bashrc

RUN bash /tmp/install_nvm.sh
RUN bash /tmp/install_node.sh

WORKDIR /usr/share/nginx/html

#CMD ["nginx", "-g", "daemon off;"]
