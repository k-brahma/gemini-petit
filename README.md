# Gemini API プチプログラム

Google の Gemini API を使用した簡単なプログラム集です。テキスト生成と画像分析の機能を提供します。

## セットアップ

### 自動セットアップ（推奨）

セットアップスクリプトを使用して、必要なパッケージを自動的にインストールできます：

- Windows: `setup.bat` をダブルクリックするか、コマンドプロンプトで実行します。
- Linux/macOS: ターミナルで `chmod +x setup.sh && ./setup.sh` を実行します。

セットアップスクリプトは以下の処理を行います：
1. Python仮想環境を作成
2. 仮想環境を有効化
3. uvをインストール
4. 必要なパッケージをインストール

### 手動セットアップ

1. Python仮想環境を作成して有効化します：

#### Windows:
```bash
python -m venv venv
venv\Scripts\activate.bat
```

#### Linux/macOS:
```bash
python -m venv venv
source venv/bin/activate
```

2. 必要なパッケージをインストールします：

#### uvを使用する場合（推奨・高速）:

```bash
# uvのインストール
pip install uv

# uvを使用してパッケージをインストール
python -m uv pip install -r requirements.txt
```

#### 通常のpipを使用する場合:

```bash
pip install -r requirements.txt
```

3. `.env` ファイルに Gemini API キーを設定します：

```
GEMINI_API_KEY=your_api_key_here
```

実際の API キーに書き換えてください。

## 使い方

プログラムを実行する前に、仮想環境を有効化してください：

#### Windows:
```bash
venv\Scripts\activate.bat
```

#### Linux/macOS:
```bash
source venv/bin/activate
```

### テキスト生成プログラム

テキスト生成プログラムを実行するには：

```bash
python gemini_app.py
```

プロンプトを入力すると、Gemini API がテキストを生成します。
終了するには `exit` と入力してください。

### 画像分析プログラム

画像分析プログラムを実行するには：

```bash
python gemini_image.py
```

画像ファイルのパスと、画像に対する質問やプロンプトを入力すると、Gemini API が画像を分析して回答します。
終了するには `exit` と入力してください。

## 注意事項

- Gemini API の利用には API キーが必要です。
- API の利用には Google の利用規約が適用されます。
- 画像分析には `PIL` ライブラリを使用しているため、対応している画像形式（JPG、PNG など）のみ使用できます。
- 仮想環境を使用することで、システム全体に影響を与えずにパッケージをインストールできます。 