# Dockerfile
FROM python:3.9-slim

# 作業ディレクトリを設定
WORKDIR /app

# 依存関係のコピーとインストール
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# アプリケーションのソースコードをコピー
COPY . .

ENV FLASK_APP=app.py
ENV FLASK_ENV=development

# アプリケーションを起動
CMD ["flask", "run", "--host=0.0.0.0"]