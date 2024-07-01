#FROM ubuntu:latest
# For demonstration of images, you are not forced to only use ubuntu:latest. In this case, we use Python version 3.9
FROM python:3.9
# This will need to match port run by uvicorn or python process
EXPOSE 8000
LABEL authors="285786"
COPY ./requirements.txt /code/requirements.txt
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt
COPY ./ /code/
# Need to designate a folder for code based on best practices: https://docs.docker.com/develop/develop-images/dockerfile_best-practices/
WORKDIR /code
# uvicorn port will need to match exposed port above
#  Test this out by running locally with docker on non-standard ports such as 81, or 8002, etc.
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]