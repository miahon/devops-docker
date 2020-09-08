FROM ubuntu:focal 

RUN apt-get update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN apt-get install -y git
RUN git clone https://github.com/miahon/fullstack-osa3.git
WORKDIR /fullstack-osa3
RUN npm install
EXPOSE 30001
CMD ["npm","start"]



