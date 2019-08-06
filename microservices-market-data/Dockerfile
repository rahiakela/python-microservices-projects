# Instructs Docker to build this image using python:3.6 as a starting point
FROM python:3.6

# Copies the current code directory to a directory /app inside the container image
ADD . /app

# Sets the working directory of the container to /app
WORKDIR /app

# install all dependencies
RUN pip install -r requirements.txt

# set the command that’ll be used to start your application
CMD ["gunicorn", "-c", "config.py", "app:app"]

# instruct Docker to expose 8000 port to app
EXPOSE 8000
