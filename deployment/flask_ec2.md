# Flask アプリ EC2 デプロイ手順

## 目的
EC2環境にPython Flaskアプリをデプロイし、Web公開する。

## 使用技術
- EC2（Amazon Linux2）
- Python
- Flask
- Nginx
- Gunicorn

## 構成イメージ

Client → Nginx → Gunicorn → Flask

## 手順

### ① EC2接続

```bash
ssh -i key.pem ec2-user@xxx.xxx.xxx.xxx