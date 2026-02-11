# GitHub Actions による CI/CD 構築

## 目的
Push時に自動テスト・デプロイを実行。

## 使用ツール
- GitHub Actions
- Python
- pytest

## ワークフロー構成

- Push
- Test
- Build
- Deploy

## 設定例

.github/workflows/python.yml

```yaml
name: Python CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Set up Python
      uses: actions/setup-python@v2
      with:
        python-version: '3.9'

    - name: Install deps
      run: pip install flask pytest

    - name: Run tests
      run: pytest
```
## 学んだこと
- 自動化で品質向上
- 人的ミス削減
- 継続的改善が可能

## 今後
- CD導入
- AWS連携