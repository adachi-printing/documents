# Adobe ExtendScript のバイナリ形式出力の手順

## Description / バイナリ形式とは

ExtendScriptはJavascriptの状態から暗号化されたバイナリ形式へ変換することができます

バイナリ変換によって、スクリプトファイルのサイズが小さくなるほか、暗号化されるためソースコードの解読が困難になります

バイナリ出力されたファイルは拡張子が.jsxbinになります

一部のAdobeアプリでは.jsxbinをスクリプトファイルとして認識しないので、拡張子を.jsxに手動で変更する必要があります

## Usage / 手順

### Adobe ExtendScript Toolkitを使用する

CSなどに付属、もしくはCreative Cloudにて”古いアプリを表示”にして表示される一覧からインストール

Extend Script toolkitで目的のスクリプトファイルを読み込んだのち、”ファイル＞バイナリ形式で書き出し”で出力

注：Toolkitは公式サポートが終了しています。また32bitアプリケーションのため、64bitマシンでは動作しません

### Visual Studio Codeを使用する

以下からダウンロードとインストールを行なってください

https://azure.microsoft.com/ja-jp/products/visual-studio-code/

VS Codeの拡張パネルからExtendScript Debuggerのプラグインをインストール

VS Codeで目的のスクリプトファイルを読み込んだのち、右クリックメニューから”バイナリとして書き出し”で出力

## ソースコードとバイナリ出力の比較

ソースコード
```javascript
/******/ (function() { // webpackBootstrap
/******/ 	var __webpack_modules__ = ({

/***/ "./node_modules/extendscript-es5-shim-ts/index.js":
/*!********************************************************!*\
  !*** ./node_modules/extendscript-es5-shim-ts/index.js ***!
  \********************************************************/
/***/ (function() {
```
改行やスペースなどがきちんと行われており、読むことができる

バイナリ化
```
@JSXBIN@ES@2.0@MyBbyBn0ABJ2lJGnAENyBnAMAbyBnABM2kOGbyBn0AFJ2kQGnASzMjDjBjDjIjFjE
iNjPjEjVjMjFBAQzACfjzYififjXjFjCjQjBjDjLifjNjPjEjVjMjFifjDjBjDjIjFififDfVzIjNjP
jEjVjMjFiJjEEfCnftO2kRGby2kSGn0ABZ2kSGnAXzHjFjYjQjPjSjUjTFfVBf0ACzDhBhdhdGVBfAj
zJjVjOjEjFjGjJjOjFjEHfnnnJ2kVGnASzGjNjPjEjVjMjFIBBQCfjDfVEfCWzGiPjCjKjFjDjUJBFW
```
改行やスペースが削除され、文字も変換されて人が読むことができない