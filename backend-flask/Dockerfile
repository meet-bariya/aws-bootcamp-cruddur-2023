FROM python:3.10-slim

WORKDIR /backend-flask

COPY requirements.txt .

RUN python -m venv /opt/venv && \
    /opt/venv/bin/pip install --upgrade pip && \ 
    /opt/venv/bin/pip install --no-cache-dir -r requirements.txt

COPY . . 

EXPOSE 4567

CMD /opt/venv/bin/python -m flask run --host 0.0.0.0 --port 4567