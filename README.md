# template_repo

![CI](https://github.com/yamanora/temp_repo/actions/workflows/ci.yml/badge.svg)  
[![codecov](https://codecov.io/gh/yamanora/temp_repo/branch/main/graph/badge.svg)](https://codecov.io/gh/yamanora/temp_repo)

開発用Pythonテンプレート  
Poetry/pre-commit/pytest(+coverage) /CI

---

## セットアップ手順

```bash
poetry install --with dev
pre-commit install
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
template_repo/
├── temp_repo/              # パッケージ本体
│   ├── __init__.py
│   └── cli.py              # CLIのエントリーポイント
├── tests/                  # 単体テスト
│   └── test_dummy.py
├── .github/workflows/ci.yml  # CI設定
├── pyproject.toml
├── README.md
└── ...
```

## TODO

- [ ] GitHub Actions 構築（pytest / coverage）
- [ ] Mermaid構成図（CLIの階層構造）
- [ ] 初回タグ付け（v0.1.0）
