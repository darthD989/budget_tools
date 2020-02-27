FROM ubuntu:18.04

RUN apt-get update -qq && \
    apt-get upgrade -qqy

RUN apt-get install -qqy \
    python-virtualenv \
    libpq-dev \
    python3=3.6.* && \
    apt-get install -y software-properties-common && \
		apt-get install -y openssh-server && \
		apt-get install openssh-client -y && \
		apt-get install -y iputils-ping && \
		apt-get install -y vim && \
		apt-get install -y tmux && \
		apt-get install -y telnet && \
		apt-get install -y sudo && \
		apt-get install -y git

RUN	apt install -y python3-pip && \ 
  	pip3 install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
COPY requirement.txt /app/
WORKDIR /app

# instruction to be run during image build
#RUN pip install -r requirement.txt
# Copy all the files from current source duirectory(from your system) to
# Docker container in /app directory 

# Specifies a command that will always be executed when the  
# container starts.
# In this case we want to start the python interpreter
# We want to start app.py file. (change it with your file name) 
# Argument to python command
#CMD [“python3 app.py”]
