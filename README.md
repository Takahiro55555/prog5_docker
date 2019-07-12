# prog5_docker

## About
プログラミング演習５の開発環境をまとめたものです。\
演習室と同じDBの設定のままでDBに接続、使用することができます。

なお、実際に使用するには[Docker](https://qiita.com/gold-kou/items/44860fbda1a34a001fc1)が必要です。\
Windowsの場合、OSのエディションによってインストールの方法が異なるみたいです。\
[Windows10 Home](https://qiita.com/idani/items/fb7681d79eeb48c05144)の場合\
[Windows10 Pro](https://qiita.com/ksh-fthr/items/6b1242c010fac7395a45)の場合\
なお、参考サイトは適当なので分からない箇所があったら適宜ググってください。

### DBサーバ
- postgresql9.2

### APサーバ・クライアント
- Ubuntu16.04

### ファイル構成
```
prog5_docker/
├── .docker #基本的に触ったらダメ
│   ├── docker-compose.yml
│   ├── postgres
│   │   └── Dockerfile
│   └── ubuntu
│       └── Dockerfile
├── Readme.md
├── mac_01_docker_start.sh            # Macで仮想マシン（コンテナ）を起動する
├── mac_02_docker_new_window.sh       # Macで仮想マシンにログインする（bash）
├── mac_03_docker_stop.sh             # Macで仮想マシンを停止する
├── windows_01_docker_start.bat       # Windowsで仮想マシン（コンテナ）を起動する
├── windows_02_docker_new_window.bat  # Windowsで仮想マシンにログインする（bash）
└── windows_03_docker_stop.bat        # Windowsで仮想マシンを停止する
```

## How to use
1. プロジェクト（作業）ディレクトリを`project`とします。
2. 作業ディレクトリに、本リポジトリ`prog5_docker`を置きます。

```
project # ここに演習用のファイルやディレクトリが置いてあると仮定
├── ex10/ # 演習のプログラムファイル
├── ex11/ # 演習のプログラムファイル
├── ex12/ # 演習のプログラムファイル
├── prog5_docker/ # このGitHubのリポジトリを丸々コピーしてくる
├── tmp.c # 演習のプログラムファイル
└── tmp.h # 演習のプログラムファイル
```

3. 仮想マシンにログインしたら、`~/work/`に移動してください。
4. 仮想マシンから、`project`ディレクトリの中のファイルを実行・編集・追加することができます。

```
work # ここに移動した
├── ex10/ # projectディレクトリにあるディレクトリ
├── ex11/ # projectディレクトリにあるディレクトリ
├── ex12/ # projectディレクトリにあるディレクトリ
├── prog5_docker/
├── tmp.c # projectディレクトリにあるファイル
└── tmp.h # projectディレクトリにあるファイル
```


OSに応じた（シェル）スクリプトを実行すると、利用できると思います。\
なお、最初に起動する際はイメージをダウンロードするため、5分ほど待機する必要があります。