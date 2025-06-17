# Polyscope の使い方

このプロジェクトは 3D データの可視化ライブラリ **Polyscope** を提供します。以下では本リポジトリの取得方法、ビルド手順、およびサンプルコードの実行方法を説明します。

## 1. リポジトリの取得

依存ライブラリは Git のサブモジュールとして管理されています。初回取得時は以下のように `--recursive` オプションを付けてクローンしてください。

```bash
git clone --recursive <repository-url>
```

すでにクローン済みでサブモジュールを取得していない場合は、次のコマンドで取得できます。

```bash
git submodule update --init --recursive
```

## 2. ライブラリのビルド

CMake を用いてビルドします。リポジトリのルートで以下を実行してください。

```bash
mkdir build
cd build
cmake ..
make
```

これにより `libpolyscope.a` などのライブラリファイルが生成されます。

## 3. サンプルコードの実行

`examples/demo-app` にサンプルアプリケーションが用意されています。以下の手順でビルド・実行してください。

```bash
cd examples/demo-app
mkdir build
cd build
cmake ..
make
./bin/polyscopedemo
```

実行するとウィンドウが起動し、登録したメッシュや点群などを操作・表示できます。

以上が基本的な使い方とサンプルコード実行までの流れです。詳細なドキュメントは公式サイト [polyscope.run](https://polyscope.run) も参照してください。
