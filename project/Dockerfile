FROM python:3.8

# copy the requirements file into the image
COPY ./techtrends/requirements.txt /app/requirements.txt

# switch working directory
WORKDIR /app

# install the dependencies and packages in the requirements file
RUN pip install -r requirements.txt

# copy every content from the local file to the image
COPY ./techtrends/ .

RUN python init_db.py

EXPOSE 3111

# configure the container to run in an executed manner
ENTRYPOINT [ "python" ]

CMD ["app.py" ]