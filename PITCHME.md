tilto

A TUI (Text User Interface) renderer

---

### 自己紹介

- 株式会社マネーフォワード
- フロントエンド周りのお仕事
- 今回の話は両方ともあんまり関係ない

---

### tilto とは

- TUI を構築するための描画エンジン
- `render(state) -> view` の `render`
- 今回 `view` に相当するのはテキスト
- star 数は 0 (三時間前に publish)

---

### TUI とは

- GUI に対しての用語
- "一般的なテキスト端末で表示できる記号や文字だけで画面を構成する" (引用: Wikipedia
- Vim とか Emacs とかそういうのだと思う

---

### モチベーション(前向き)

こういうゲームが好き。（画像は [変愚蛮怒公式サイト](http://hengband.osdn.jp/) より）

![](/hengband.png)

---

### モチベーション(後向き)

- 手軽に動かせるものが好き
- だからフロントをやっている
- でもビルドめんどい
- percel すらめんどい

---

## 錯乱

ターミナルで

動くものを作ればいいんだ！

---

### どんな感じ

```js
const tilto = require('tilto');

// 枠を作る
let box = tilto.createBox({width: 20, height: 5});
// 枠線をつける
box = tilto.setBorderType(box, 'default');
// コンテンツを定義する
box.content = 'The quick brown fox jumps over the lazy dog.';

// render でテキスト化
console.log(tilto.render(box));
// -> +------------------+
//    |The quick brown fo|
//    |x jumps over the l|
//    |azy dog.          |
//    +------------------+
```

---

## よんまいめ(h2)

---

# ごまいめ(h1)

---

### いちまい足りない・・・
