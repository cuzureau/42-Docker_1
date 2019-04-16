# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: cuzureau <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/08/13 14:50:01 by cuzureau          #+#    #+#              #
#    Updated: 2018/08/13 14:56:40 by cuzureau         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

RUN apt upgrade -y && \
    apt update -y && \
    apt install wget -y

RUN useradd ts3 && \
    su ts3

RUN wget http://ftp.4players.de/pub/hosted/ts3/releases/3.0.7/teamspeak3-server_linux-amd64-3.0.7.tar.gz && \
    tar -zxvf teamspeak3-server_linux-amd64-3.0.7.tar.gz

EXPOSE 9987/udp 10011 30033

WORKDIR /teamspeak3-server_linux-amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh
