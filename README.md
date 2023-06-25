# rp2040_1.28_touch_LCD

rp2040を搭載したLCDの挙動テスト

円を描画、タッチ、スワイプ時の挙動を一通りテストした
起動時に円を描画して画面に縁を追加するアニメーションを入れている

LCDというクラスを作成して以下のドキュメントにある機能を使用している。
https://micropython-docs-ja.readthedocs.io/ja/latest/library/framebuf.html#

LCD.textではフォントの大きさの変更はできないが、LCD.write_textというメソッドでフォントを拡大してテキスト表示が可能

```
LCD.write_text("text", x, y, size, color)
```

画面左右スワイプ、ダブルタップ、長押しでX→Y→Zと計測軸が変わる
