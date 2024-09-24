FROM python:3.11.4-bookworm 

RUN pip install --upgrade pip

EXPOSE 8888

WORKDIR /problem5

COPY requirements.txt .

RUN pip install -r requirements.txt

CMD ["jupyter-lab", "--allow-root"]