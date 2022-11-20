---
title: "Linuxコマンド"
date: 2022-11-02T11:03:16+09:00
---

## 基本
- `pwd`<br>: カレントディレクトリの絶対パス
- `ls`<br>: カレントディレクトリにあるファイル
- `cd`<br>: ディレクトリ移動
- `mkdir`<br>: ディレクトリ新規作成
- `touch`<br>: ファイル新規作成（普段はnanoでやってる）
- `mv`<br>: `mv source/path destination/path`で移動、`mv before_name after_name`でリネーム（Windowsではできなかった記憶がある）
- `cp`<br>: ファイルのコピー。`-r`でディレクトリをコピー。
- `rm`<br>: `-f`で強制削除、`-r`でディレクトリ以下を削除
- `wc`<br>: 行数カウント。`-l`でファイル名も表示。
- `cat`<br>: ファイルの中身を標準出力
- `head/tail -n x`<br>: ファイルの先頭/末尾x行を標準出力
- `sort`,`uniq`<br>: 行単位でソート、重複行の削除
- `grep str file`<br>: fileからstrを含む行を抽出
	- `grep str -rl PATH`<br>: 中身にstrが含まれているファイルを再起的に取得
- `sed -e 's/BEFORE/AFTER/g' file`<br>: ファイル中の文字を置換。`-i`で上書き。
- `less`<br>: ファイル閲覧
- `du`<br>: ファイルの容量表示。`-h`でちょうどいい単位にしてくれる。`--max-depth N`で階層指定。
- `ps`<br>: いまターミナルで実行中のプロセスを表示

## ショートカット
- <kbd>Ctrl</kbd>+<kbd>A</kbd>, <kbd>Ctrl</kbd>+<kbd>E</kbd><br>: 行頭、行末へカーソル移動
- <kbd>Ctrl</kbd>+<kbd>U</kbd>, <kbd>Ctrl</kbd>+<kbd>K</kbd><br>: 行頭、行末まで削除
- <kbd>Ctrl</kbd>+<kbd>W</kbd><br>: 1単語分のコマンドを削除
- <kbd>Ctrl</kbd>+<kbd>C</kbd><br>: 実行中のプロセスを中断

## 解凍・圧縮
- ファイルの解凍・圧縮
	- 圧縮: `gzip file`
	- 解凍: `gunzip file.gz`
	- ディレクトリ下のファイル全て: `gzip directory/*`
- ディレクトリごと
	- 圧縮: `tar czf directory.tar.gz directory`
	- 解凍: `tar xzf directory.tar.gz`

