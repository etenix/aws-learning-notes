# EC2 インスタンス構築手順

## 使用環境
- OS：Amazon Linux 2
- インスタンスタイプ：t2.micro
- リージョン：ap-northeast-1（東京）
- 接続方式：SSH

## 構築目的
Flask を利用した簡易Webアプリの動作確認環境を構築するため。

## 構築手順

1. AWSマネジメントコンソールにログイン
2. EC2サービスからインスタンスを作成
3. Amazon Linux 2 を選択
4. キーペアを作成・保存
5. セキュリティグループ設定
   - SSH：22番ポート
   - HTTP：80番ポート
6. インスタンス起動確認

## 接続方法

```bash
ssh -i key.pem ec2-user@xxx.xxx.xxx.xxx