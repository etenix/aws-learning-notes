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
```
### ② Python環境構築

```bash
sudo yum install python3 -y
pip3 install flask gunicorn
```

### ③ アプリ配置

```bash
git clone https://github.com/username/simple-web-app-python.git
cd simple-web-app-python
```

### ④ Gunicorn起動

```bash
gunicorn app:app
```

### ⑤ Nginx設定

```bash
sudo yum install nginx -y
sudo systemctl start nginx
```

## 学んだこと
- 本番環境ではFlask単体起動は不十分
- Nginxとの連携が重要
- プロセス管理の必要性

## 改善点
- systemd登録
- 自動起動設定
- HTTPS対応