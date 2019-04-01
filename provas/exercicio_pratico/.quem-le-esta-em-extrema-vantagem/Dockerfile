FROM centos
WORKDIR /opt/app

# Install Python Dependecies
RUN yum install -y epel-release && \
		yum install -y wget && \
		yum install -y gcc && \
		yum install -y make && \
		yum install -y python-pip

# Install Python 2.7
RUN	wget https://www.python.org/ftp/python/2.7.15/Python-2.7.15.tgz && \
	  tar xzf Python-2.7.15.tgz && \
	  cd Python-2.7.15 && \
		./configure --enable-optimizations && \
		make altinstall

# Install requirements
COPY requirements.txt /opt/app/
RUN pip install -r requirements.txt

# Copy application
COPY app.py /opt/app/

EXPOSE 8000
CMD ["python","app.py"]
