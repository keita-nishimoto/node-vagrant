# nodejs_mongodb.provision

# 概要

Node.jsのテスト用環境です。

[nodejs_mongodb.playbook](https://github.com/keita-nishimoto/nodejs_mongodb.playbook)とセットで利用します。

現状以下のプロジェクトが動作します。

- [react_tutorial_es5](https://github.com/keita-nishimoto/react_tutorial_es5)
- [react_tutorial_es6](https://github.com/keita-nishimoto/react_tutorial_es6)

# 使い方

関連Repositoryを入手し、以下のように全て同階層に配置して下さい。

```
├ react_tutorial_es6
├ nodejs_mongodb.playbook
├ nodejs_mongodb.provision
```

以下のコマンドを実行するとVagrantBOXに対してAnsibleのprovisioningが実行され環境構築が行われます。

# 注意

前提条件として、ansible 1.9.2以上、VirtualBoxがインストールされている必要があります。
インストールがまだの場合は以下の手順でインストールを行って下さい。

①Homebrewをインストール

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

②Ansibleをインストール

```
brew install ansible
```

③VirtualBox
https://www.virtualbox.org/ よりダウンロードを行いインストールして下さい。


# 実行方法

プロジェクトルートで以下のコマンドを実行して下さい。
必要なパッケージをインストールします。
