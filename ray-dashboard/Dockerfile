FROM ubuntu:18.04
RUN apt-get update && apt-get install -y nodejs \ 
    npm \ 
    build-essential \
    python3.7 \
    python3-pip
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3 10
RUN pip3 install ray[dashboard] psutil setproctitle
WORKDIR /app
COPY ./initialize_ray_dashboard.py /app
EXPOSE 8265
CMD ray start --head --block --webui-host 0.0.0.0
