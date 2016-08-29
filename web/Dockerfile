FROM debian:wheezy
MAINTAINER Andrew Huynh <andrew@productbio.com>
RUN apt-get update && apt-get install -y \
            python-dev python-pip python-setuptools \
            libffi-dev libxml2-dev libxslt1-dev \
            libtiff4-dev libjpeg8-dev zlib1g-dev libfreetype6-dev \
            liblcms2-dev libwebp-dev tcl8.5-dev tk8.5-dev python-tk

COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
ENTRYPOINT ["python"]
CMD ["app.py"]
