# temp-repo

![CI](https://github.com/yamanora/temp-repo/actions/workflows/ci.yml/badge.svg)  
[![codecov](https://codecov.io/gh/yamanora/temp-repo/branch/main/graph/badge.svg)](https://codecov.io/gh/yamanora/temp_repo)

開発用Pythonテンプレート  
Poetry/pre-commit/pytest(+coverage) /CI

---

## セットアップ手順

```bash
# 仮想環境を構築（dev依存も含めてインストール）
poetry install --with dev

# pre-commitを仮想環境から実行・インストール
poetry run pre-commit install
```

---

## 使い方（例）

CLI モジュールが定義されている場合：

```bash
poetry run temp-repo --help
```

---

## ファイル構成

```
temp-repo/
├── src/
│   └── temp_repo/          # パッケージ本体
│       ├── __init__.py
│       └── cli.py          # CLIのエントリーポイント
├── tests/                  # 単体テスト
│   └── test_dummy.py
├── .github/
│   └── workflows/
│       └── ci.yml          # CI設定
├── pyproject.toml
├── README.md
└── ...
```

---

処理構成のイメージ（Mermaid）：

```mermaid
flowchart TD
    A[cli.py] --> B[argparseで引数解析]
    B --> C[handler関数に分岐]
    C --> D1[format_csv]
    C --> D2[summarize_csv]
    D1 --> E1[出力ファイル保存]
    D2 --> E2[出力ファイル保存]
```
