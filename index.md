% header
title: Gitっておいしいの？

author: Takuya

% slide
#Gitとは？

分散型バージョン管理システム

リーナス・トーバルズがLinuxのソース管理のために開発



#分散型じゃないバージョン管理システムといえば

* Subversion

  シーポイントおなじみのバージョン管理システム

  svn.cpt.jpに対してcommitやupdateを行う。

* オンライン必須



# 分散型の利点

* リモートレポジトリとローカルレポジトリが存在

* commitはローカルレポジトリの更新→オンラインでなくてもコミットが可
* 開発中のコミットがほかの人へ影響されない
* リモートを更新するにはPushを行う。

# Gitの利点

* コミット内容を後から修正可能
* オフラインでも使える
* ブランチやタグの操作が高速

# Gitの問題
ブランチが作りやすいからということでブランチの乱立

ブランチ管理をちゃんと行わないとこの修正点がめちゃくちゃに

* Github-flow
* git-flow

# git-flow

A successful Git branching modelを実現するためのコマンド

ブランチの自由度をなくすことでわかりやすく

# メインブランチ
  *master
  *develop

# master
  リリース済みの最新ソースがあるブランチ

  CLOGで言えばfs11に上がっているソース

  わざわざFTPで取りにいかなくてもブランチをmasterにすれば最新ソースが見れる

# develop

  最新の開発版ブランチ

  次期リリース版など

  demo.clog3.netはここと同じにする

# サポートブランチ

  * Feature
  * Release
  * Hotfix

# Featureブランチ

  新規機能開発ブランチ

  機能ごとに作成

  分岐元:develop

  マージ先:develop

# Releaseブランチ

  バージョンコードなどを変更するブランチ

  リリース作業に必要な細かな作業を行うブランチ

  使わないチームも多いらしい

  分岐元:develop

  マージ先: master develop

# Hotfixブランチ
  bugfixブランチ

  最新のソースに不具合があった場合に仕様するブランチ

  分岐元: master

  マージ先: master

# git-flowはこのブランチモデルを簡単に使えるコマンド群

[git-flow cheatsheet](http://danielkummer.Github.io/Git-flow-cheatsheet/index.ja_JP.html)

# コマンドうつのめんどくさい

GUIあるよ！
* [SourceTree](https://www.atlassian.com/ja/software/sourcetree/overview)
  git-flowも使える便利なGUI
* [TortoiseGit](https://code.google.com/p/tortoisegit/)
  TortoiseSVNのGit版
* [GitHub for Windows](https://windows.github.com/)
  Gitといえば[GitHub](https://github.com/)

# GithubとGitLab

[GitHub · Build software better, together.](https://github.com/)

[Create, review and deploy code together | Better than GitHub | GitLab](https://about.gitlab.com/)

[シーポイントのGitLab](http://gitlab.tida-square.co.jp)

# さあGitを使ってみよう！

[Code School - Try Git](https://try.github.io/levels/1/challenges/1)
