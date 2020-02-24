FROM ubuntu:18.04

RUN apt-get update -qq && \
    apt-get upgrade -qqy

RUN apt-get install -qqy \
    python-virtualenv \
    libpq-dev \
    python3=3.6.* 

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
#CMD [“python app.py”]
