FROM python:3.10-slim-buster

#Insider 
# make new folder inside container
WORKDIR /backend-flask

# Inside Container => Outside Container
# contains liabries for the app run
COPY requirements.txt requirements.txt

#Insider Container
# Install Python liabries 
RUN pip3 install -r requirements.txt

# Inside Container => Outside Container
# everything current directory. insider and outsider backend-flask
COPY . .

# ENV VARS
#inside container
ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]