# Adobe ExtendScript のバイナリ形式出力の手順

## Description / バイナリ形式とは

ExtendScriptはJavascriptの状態から暗号化されたバイナリ形式へ変換することができます

バイナリ変換によって、スクリプトファイルのサイズが小さくなるほか、暗号化されるためソースコードの解読が困難になります

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

