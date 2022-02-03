---
title: アップデート方法 
description: '限界大会公式ドキュメント、wiki.genkai.workへようこそ！'
position: 2
category: guide
version: 1
fullscreen: false
---

damareでは、しばしばアップデートが行われます。      
現時点では自動アップデート機能や、アップデート確認機能はありません。

そのため、定期的に以下のコマンドを実行してください。

```powershell
git pull
```

`Already up to date.` と表示された場合は、すでに最新なのでなにもする必要はありません。

それ以外が表示された場合、アップデートされたことになります。        
その場合、以下のコマンドを実行します。

```powershell
yarn install
```

これで更新された依存関係をインストールすることができます。      
あとはいつもどおり起動すればOKです。