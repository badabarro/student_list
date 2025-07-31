FROM python:3.8-bookworm
LABEL maintainer="Badaoudou BARRO"
COPY requirements.txt student_age.py /
RUN apt-get update && apt-get install -y \
    python3-dev \
    libsasl2-dev \
    libldap2-dev \
    libssl-dev && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

RUN pip3 install -r /requirements.txt
VOLUME ["/data"]
EXPOSE 5000
CMD ["python3", "./stutent_age.py"]