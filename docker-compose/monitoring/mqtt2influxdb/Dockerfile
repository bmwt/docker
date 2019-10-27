FROM python:3.7-alpine
COPY mqtt_to_influxdb.py /
COPY mqtt_to_influxdb.conf /
COPY requirements.txt /
RUN pip install -r /requirements.txt
CMD ["python3", "./mqtt_to_influxdb.py"]
