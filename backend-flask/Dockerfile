FROM python:3.10-slim-buster

# Container
WORKDIR /backend-flask

# Outside Container --> Inside Container
# This contains the libraries we want to install to run the app
COPY requirements.txt requirements.txt

# Install the python  images used in the app Inside Container
RUN pip3 install -r requirements.txt


# Outside Container --> Inside Container
# This contains the app code
# . meanseverything in the current dir.
# First period is /backend-flask (Outside Container)
# Second Period is 
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
# CMD used to run flask
# CMD [ python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]