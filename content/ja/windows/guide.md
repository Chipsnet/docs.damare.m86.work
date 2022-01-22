---
title: セットアップ手順 
description: '限界大会公式ドキュメント、wiki.genkai.workへようこそ！'
category: Windows
position: 1
version: 1
fullscreen: false
items:
    - Windows (10以上)
    - Node.js
    - Yarn
    - Git
---

## 動作に必要な前提条件

以下がインストールされている必要があります。

<list :items="items"></list>

## Node.jsのインストール

Node.jsのダウンロードサイトにアクセスし、LTS（推奨版）のWindows Installerをダウンロードします。

https://nodejs.org/ja/download/

![](https://i.gyazo.com/f924a75f198d22a63a5b6645efd629b3.png)

ダウンロードしたファイルを実行し、手順に従ってインストールします。

## Yarnのインストール

Node.jsをインストールした後

```bash
npm install -g yarn
```

とWindows Powershellで実行してインストールします。

## Gitのインストール

Gitのダウンロードサイトにアクセスし、以下の画像のボタンをクリックしてインストーラーをダウンロードします。

https://git-scm.com/

![](https://i.gyazo.com/bde99a6d0af5ca43dd49cfb009fb4849.png)

ダウンロードしたファイルを実行し、手順に従ってインストールします。

<alert type="info">

インストール時にいろいろな選択肢が出てきますが、すべて次へ（Next）で大丈夫です。

</alert>

## Discord Bot Tokenを取得する

Botを動かすためにはToken（トークン）というものをDiscordから取得する必要があります。

取得方法は以下の記事を参考にしてください。      
https://cod-sushi.com/discord-py-token/

## 音声合成エンジンを選択する

Damareは、様々な場面で利用できるように、音声合成エンジンを選択できるようになっています。

現在利用可能なのは以下の2つです。

- Softalk
    - セットアップがとても簡単だが遅延がすこしある。カスタマイズ性もあまりない。
- OpenJTalk
    - セットアップが難しいが低遅延。カスタマイズがかなり豊富にできる。