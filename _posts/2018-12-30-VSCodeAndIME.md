---
layout: post
title:  "Visual Studio CodeのVimにおけるIMEのON/OFF"
date:   2018-12-31 03:43:06 +0900
categories: vim
---
本家Vimの"+multi_byte_ime"と同じように、normal modeにするとIMEがOFFになり、再度insert modeにすると前の状態を復元する[設定][ime-setting]ができる。IME ONで入力していたらならONに戻るので、日本語の入力も快適である。

## 準備
* Windowsの入力言語として英語(US)を追加しておく
* 英語入力時のキーボードをUSから日本に変更しておく
* IME入力モードの切り替えの通知も、画面中央にいちいち表示されて邪魔なので、IMEのプロパティでOffにしておく
* 上記の設定に従ってVSCodeVimのSettingとim-selectの導入を行う

## 補足
Googleの日本語ページ検索結果にはまっとうな対応方法が見つけられなかったので書いておく。中国語にも同じ[課題](https://github.com/VSCodeVim/Vim/pull/2643)があるため、対応が進んだようだ。

IMEを切り替えるたびに実行ファイル"im-select.exe"を呼び出すためか、少し反応が鈍いのが玉に瑕ではある。

[ime-setting]: https://github.com/VSCodeVim/Vim#input-method
