# FROM python:3.10
FROM python:3.10

WORKDIR /app/

RUN pip install --upgrade pip setuptools wheel
RUN pip install --index-url=https://pkgs.dev.azure.com/azure-sdk/public/_packaging/azure-sdk-for-python/pypi/simple/ azure-search-documents==11.4.0a20230509004
RUN pip install azure-identity

# req.txtからパッケージをインストール
COPY requirements.txt /root/app/requirements.txt
RUN pip install -r /root/app/requirements.txt

CMD ["gradio", "main.py"]
