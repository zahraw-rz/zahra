FROM python:3.12.3

WORKDIR /fastapi

COPY ./requirements.txt /fastapi/

RUN pip install -r /fastapi/requirements.txt

COPY  . /fastapi

CMD ["fastapi", "run", "main.py", "--port", "80"]