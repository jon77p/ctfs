FROM ubuntu:latest

LABEL maintainer="jon77p@gmail.com"

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install ssh -y
RUN apt-get install sshpass -y

ENV CTF_URL bandit.labs.overthewire.org
ENV CTF_PORT 2220

ENTRYPOINT sshpass -e ssh -o StrictHostKeyChecking=accept-new "$CTF_USER"@"$CTF_URL" -p "$CTF_PORT" "$CTF_CMD"
