FROM python:3

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirement.txt

COPY . .
EXPOSE 5000
CMD [ "python", "./app.py" ]
