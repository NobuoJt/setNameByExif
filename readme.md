# ViRPE - View image, Rename and Proceed by EXIF

変な名前してるけど、ただの個人用ツール。  
pythonほとんど使ってないのでChat GPTくんに助けを借りてGUIツールを作ってみた。  
いちおう読みは「バープ」で。

なんかEXEにコンパイルしようとしてもwindows defenderに阻まれて動かないのでpy上で動かすことにします。()

## Feature / Usage

![alt text](image.png)  
パスのスペル間違えてるのは目をつぶってくれ  

### Component

|上部ボタン||
|-|-|
|フォルダ選択| ```./config.dat``` の1行目を基準にフォルダ選択のウィンドウが出る。
|リネーム(from textbox)|上部テキストボックスのとおりに選択ファイル名が改名。(拡張子含まず)
|リネーム(add EXIF)|シャッタースピード、F値、iso、焦点距離を選択ファイル名に追加。|
|copyToClip(EXIF)|選択ファイルのEXIF情報を上部テキストボックスに表示、クリップボードにコピー。
|excel|外部コマンド1。```./config.dat```の2行目で指定。
|share folder|外部コマンド2。```./config.dat```の3行目で指定。

|コンテンツ||
|-|-|
|上部テキストボックス|操作指示、拡張子なしファイル名、exif情報を表示。ファイル名変更も可能。|
|画像ファイルリスト|マウスで選択、全体表示。|
|画像表示エリア|マウスクリックで全体の2倍で表示。|

### Download

このソースを全部コピーしてpython叩く(or .bat)か、  
```dist/ViRPE_lite.exe``` を動かすか。  

ただしViRPE_liteは機能を削減した上にWindows Defenderに怒られながら産んだのであまりおすすめはしない。

### Memo

```./HelloWorld.py```の5行目は優秀な助手:Chat GPTのリンク