FROM python:3.5
RUN mkdir -p /app/user
RUN mkdir /src
WORKDIR /app/user
ADD requirements.txt /app/user/
RUN pip install --upgrade pip
RUN pip install --src /src -r requirements.txt
ADD . /app/user
RUN python ./manage.py collectstatic --noinput
EXPOSE 8000
