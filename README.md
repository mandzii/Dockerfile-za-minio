# Base image
FROM ubuntu:21.10
# Expose port 9001
EXPOSE 9001
# Install wget
RUN apt-get update && apt-get install -y \
    wget
RUN cd /tmp
# Taken from "https://min.io/download#/linux"
RUN wget https://dl.min.io/server/minio/release/linux-amd64/minio
RUN chmod +x minio
RUN MINIO_ROOT_USER=admin MINIO_ROOT_PASSWORD=password ./minio server /mnt/data --console-address ":9001"

kad pokrenes
docker build .
pisace ti
console: http://ip-adresa:9001
i tamo ides
i imaces minio
