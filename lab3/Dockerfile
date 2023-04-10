FROM python:3.10
WORKDIR /model
run ls -la
COPY lab3/requirements.txt ./requirements.txt
RUN pip3 install -r requirements.txt
COPY . .
CMD ["python", "./main.py"]
