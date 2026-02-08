# S3 ファイルアップロード実践

## 目的
AWS S3を利用したファイル保存・公開方法の理解。

## 実施内容

- バケット作成
- ファイルアップロード
- アクセス権限設定
- 公開URL確認

## 使用環境

- AWS Management Console
- AWS CLI

## 操作手順

1. S3バケット作成
2. リージョン設定（東京）
3. ファイルアップロード
4. パブリックアクセス設定
5. URLからアクセス確認

## AWS CLI 使用例

aws s3 cp sample.txt s3://my-bucket-name/