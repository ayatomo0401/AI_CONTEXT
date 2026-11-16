# セットアップ

Windows / PowerShell / Python 3.13を前提とする。

プロジェクトのルート（`app` フォルダが存在する場所）で実行する。

```powershell
py -3.13 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
```

有効化が拒否された場合、仮想環境のPythonを直接利用できる。

```powershell
.\.venv\Scripts\python.exe -m pip --version
```

`requirements.txt` が存在する場合:

```powershell
python -m pip install -r requirements.txt
```

`.env` の項目名は実際の `config.py` や `.env.example` と照合して設定する。GrokのAPIキーをGitHubに登録しない。モデル名や取引パラメータは未照合のため固定値を記載しない。

## 起動・確認

```powershell
python -m py_compile .\app\dashboard.py
python -m streamlit run app/dashboard.py
```

Botの起動候補（実際のCLI定義を確認してから使用）:

```powershell
python -m app.bot --once
```

資産履歴の確認:

```powershell
python -c "from app import db; print(db.query('SELECT * FROM equity_history ORDER BY id DESC LIMIT 5'))"
```

ペーパーモードであることを起動前に確認する。実取引権限のあるキーは使用しない。
