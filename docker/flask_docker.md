### 📄 内容

```md
# Flask アプリ Docker 化

## 目的
開発環境を統一し、環境差異をなくす。

## 使用技術
- Docker
- Dockerfile
- Docker Compose

## Dockerfile 例

```dockerfile
FROM python:3.9

WORKDIR /app

COPY . .

RUN pip install flask

CMD ["python", "app.py"]

## ビルド・起動
```bash
docker build -t flask-app .
docker run -p 5000:5000 flask-app
```

## 学んだこと
- 環境構築が高速化
- 再現性が向上
- チーム開発に有効

## 課題
- イメージサイズ削減
- 本番対応設定