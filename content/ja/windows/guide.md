---
title: セットアップ手順 
description: '限界大会公式ドキュメント、wiki.genkai.workへようこそ！'
category: Windows
position: 2
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

## Botのファイルをダウンロードする

Gitを使用して、Bot本体をダウンロードします。

Botのファイルを置きたい場所で

```powershell
git clone https://github.com/Chipsnet/damare.git
```

を実行します。

## 音声合成エンジンのセットアップ

Damareでは、2つの合成音声エンジンから選択して使うことができます。       
どちらも無料で利用できますが、セットアップの難易度やカスタマイズ性に違いがあります。

### Softalk

所謂「ゆっくりボイス」を生成できるソフトウェアです。        
セットアップは簡単ですが、カスタマイズ性があまりありません。

気軽に使いたい方におすすめです。

<details><summary>セットアップ方法を確認する</summary>

## Softalkをダウンロードする

VectorのSoftalkのページへアクセスし、Softalkをダウンロードします。

http://www.vector.co.jp/soft/winnt/art/se412443.html

![](https://i.gyazo.com/d25dee33364ffa6ac2679190fcd71522.png)

ダウンロードしたSoftalkを解凍し、でてきた`softalk`フォルダを`damare`のフォルダに入れます

![](https://i.gyazo.com/a0ad5e4413e63765eb46a1597fa34dce.jpg)

## Softalkを設定する

Softalkのフォルダに入っている `SofTalk.exe` を実行して、Softalkを起動します。

次に`オプション`から`環境変数`を開きます。

![](https://i.gyazo.com/a19435f44264640bbc57a80038a4922d.png)

`録音`タブを開き、`録音時は読み上げを省略する`にチェックを入れます。

以上の設定ができたら、Softalkを終了します。

</details>

### OpenJTalk

Softalkよりも流暢な音声を生成できますが、セットアップが少しむずかしいです。     
カスタマイズ性に優れており、htsvoiceを差し替えることで別の音声に変更ができます。

<details><summary>セットアップ方法を確認する</summary>

現在作成中です

</details>

## Configファイルの作成