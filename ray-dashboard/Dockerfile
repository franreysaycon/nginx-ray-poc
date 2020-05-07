FROM ubuntu:18.04
RUN apt-get update && apt-get install -y nodejs \ 
    npm \ 
    build-essential \
    python-pip
RUN pip install ray psutil
WORKDIR /app
COPY ./initialize_ray_dashboard.py /app
CMD python initialize_ray_dashboard.py
