## Web~~USB~~ Serial APIを使ったmicro:bitとの通信
詳細→ https://hackmd.io/@maple117/rJTVJclIO

WebUSB API(Web Serial API)を使ってウェブブラウザとmicro:bitとの通信(シリアル通信)を行うのが目的です。

## WebUSB API
web.htmlについてですが、dap.umd.jsが無いと動きません
https://github.com/ARMmbed/dapjs ←ここから手に入れてください
入手方法とかはhackmdに書いてあります。

## WebSerialAPI始めました
接続時に設定するボーレートは9600にしてください。(micro:bitのシリアル通信のデフォルトは115200)
/WebSerialAPI/webserial.html を使ってください。

## micro:bit
始めはmakecodeでコーディングしていましたが、チェックサムの実装後はc++で行うことに変更しました。
/microbit/main.cppを使ってください。
~~チェックサムに異常があった時の挙動を試したいときはNGcheck_main.cpp を使うと強制的に異常を起こせます。(送信データは33文字以上入力してください)~~
