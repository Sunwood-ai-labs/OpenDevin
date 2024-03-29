FROM ghcr.io/opendevin/sandbox:v0.1

WORKDIR /app

RUN apt update -y 
RUN apt install -y iputils-ping net-tools

COPY . .
RUN pip install -r requirements.txt      

RUN curl -fsSL https://get.docker.com -o get-docker.sh
RUN sh get-docker.sh