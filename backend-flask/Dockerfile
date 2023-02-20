FROM python:3.10-slim-buster
#inside the container make a new folder inside the cotainer
WORKDIR /backend-flask
#outside the container ---> Inside the container
COPY requirements.txt requirements.txt
# run this inside the container
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]