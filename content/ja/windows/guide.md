---
title: セットアップ手順 
description: '限界大会公式ドキュメント、wiki.genkai.workへようこそ！'
category: Windows
position: 3
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

## OpenJTalkのセットアップ

以下の記事を参考に、OpenJTalkをセットアップします。     
https://qiita.com/mkgask/items/0bf9c26dc96e7b0b45ac

なお、hts_voiceと辞書データ（dic）に関しては、damare本体に同梱されているためセットアップの必要はありません。

OpenJTalkは `open_jtalk` コマンドで実行できるようにパスを通してください。

以上でセットアップは完了です。

</details>

## Configファイルの作成

![](https://i.gyazo.com/0aa51c8cfa7735e0462f1ed9d206f836.png)

`damare` のフォルダに `config.yml` を作成して、中身を以下のようにします。

```yml
token: 取得したDiscord Token
useguild: 使用するDiscordサーバーのguild Id
prefix: prefix
voiceclient: softalk = 1, openjtalk = 2
```

### token

[Discord Bot Tokenを取得する](#discord-bot-tokenを取得する)で取得したTokenを入力します。

### useguild

使用するDiscordサーバーのguild Id(サーバーID)を入力します。     
取得方法は[公式ガイド](https://support.discord.com/hc/ja/articles/206346498-%E3%83%A6%E3%83%BC%E3%82%B6%E3%83%BC-%E3%82%B5%E3%83%BC%E3%83%90%E3%83%BC-%E3%83%A1%E3%83%83%E3%82%BB%E3%83%BC%E3%82%B8ID%E3%81%AF%E3%81%A9%E3%81%93%E3%81%A7%E8%A6%8B%E3%81%A4%E3%81%91%E3%82%89%E3%82%8C%E3%82%8B-)を御覧ください。

### prefix

コマンドの前に付く識別子です。      
例えばprefixに `;` を選ぶと、喋り始めるコマンドは `;talk` になります。

### voiceclient

使用する音声合成エンジンを選択します。      
Softalkを使う場合は`1`を、openjtalkを使う場合は`2`を入力します。

## 起動する

`damare` のフォルダで次のコマンドを実行します。

```powershell
yarn install
```

これで実行に必要なファイルが自動ダウンロードされます。      
そして

```powershell
yarn start
```

で起動します。

## アップデートする

[こちら](/guide/update)を御覧ください。