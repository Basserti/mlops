FROM python:3.10
WORKDIR /model
RUN ls -la
COPY requirements.txt ./requirements.txt
RUN pip3 install -r requirements.txt
COPY . .
CMD ["python", "./main.py"]
