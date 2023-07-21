# The original image can be any Python version according to your usage.
FROM python:3.8-bullseye

RUN apt-get update && apt-get install -y \
    nodejs \
    npm

RUN npm install -g @anthonychu/funcvm && funcvm use 3

# Specifies the working directory in the container. This can also be changed as desired.
# However, it must match the destination directory name specified in the following COPY command.
WORKDIR /app

# Copy the requirements.txt and run pip install.
ADD ./requirements.txt /app
RUN pip install -r requirements.txt

