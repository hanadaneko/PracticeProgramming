# 講座で利用するツール一覧

- IDE
  - VSCode
- git
  - git
  - Github
  - SourceTree

# 導入

## VSCode

[ダウンロードサイト](https://code.visualstudio.com/download)からダウンロード＆インストール

## GitHub

[こちら](https://github.co.jp/)から登録&ログイン

## SourceTree

[こちら](https://www.sourcetreeapp.com/)からダウンロード＆インストール

## git

### WINDOWS の場合

[こちら](https://qiita.com/T-H9703EnAc/items/4fbe6593d42f9a844b1c)参照

### MAC の場合

<details><sammary>

```
# gitが入っているか確認（おそらくMacに紐づいたものがインストールされているはず）
## 例）git version 2.24.3(Apple Git-128)
git -v

# Homebrewが入っているか確認
# HomebrewとはMac用のパッケージマネージャー
brew -v

# Homebrewが入っていない場合下記コマンドを実施
# Homebrew HP: https://brew.sh/
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Homebrewがインストールできたか確認
brew -v

# Gitのインストール
brew install git

# インストールできたか確認
brew info git

# gitのバージョンを確認
# この時点では表示されるverに変更はない。
git -v

# ------------
#　現在MacOSに直接ダウンロードされているGitと、
#  Homebrew上にダウンロードされているGitが両立し、MacOS側のが優先されている
#  Homebrew上にダウンロードされているのをデフォルトで使用するためにOSの設定ファイルを操作する
#  これを「PATHを通す」と表現する
# ------------

# SHELLを確認(zsh or bash)
# SHELLとは、コマンドをパソコンに伝えるためのシステム・プログラムのこと
echo $SHELL


# PATH Fileを開く（SHELLにGitのコマンドが来たら、Homebrewの方を利用してねと設定する）
## zshの場合
vi ~/.zshrc
## bashの場合
vi ~/.bash_profile

# インサートモードにする
# iキーを押下

# HomebrewのGitを使うパスを挿入
export PATH=/usr/local/bin/git:$PATH

# インサートモードは終了
# Escキーを押下

# 変更を保存する
:wq

# 無事に保存できたか確認
## zshの場合
vi ~/.zshrc
## bashの場合
vi ~/.bash_profile

# 無事に追加できた場合には、保存せずに終了
:q

# SHELLを再起動する
exec $SHELL -l

# gitのバージョンを確認
git -v

# バージョンが(Apple Git-128) の様な表記がないものになっていればOK
```

</sammary>
