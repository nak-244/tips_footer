# 🚀 コピペでOK！HTML・CSSでつくる汎用footerテンプレート

## 🧩 Footerテンプレートについて

### 主な使用プロパティ
- `display`
- `gap`
- `grid-template-columns`
- `margin`
- `padding`

---

### 💡 概要

footerのデザインって、どのサイトでも似ていたり、構成がほとんど同じだったりしますよね。  
そこで、**「とりあえずサクッとfooterを作りたい」** というときに使えるテンプレートを用意しました。

Tailwind CSS や Bootstrap などのフレームワークは使用せず、  
**シンプルなHTMLとCSSだけ** で構成しています。

---

### 🎨 カスタマイズについて

- 細かなスタイル指定はサイトによって異なるため、**環境に合わせて自由に編集してください。**  
- わかりやすくするために **色指定** をしています。不要な場合や変更したい場合は簡単に調整できます。  
- **クラス名は仮のもの** なので、プロジェクトの命名ルールに合わせて変更してください。

---

### 📱 レスポンシブ対応

レスポンシブ対応済みです。  
ブラウザの幅を広げたり縮めたりしながら、デザインの変化をご確認ください。

---

### 🧾 注意事項

このテンプレートはあくまで **ベースとなる構造** を示したものです。  
最終的なレイアウト・フォント・カラーなどは、実際のサイトトーンに合わせて調整してください。

---
## 🧱 シンプルなフッターテンプレート

もっとも基本的なレイアウトのフッターです。  
シンプルで使いやすく、ナビゲーション項目数や文字数に応じて微調整するだけで対応できます。

---

### 💻 HTML

```html
<footer class="footer">
  <ul class="md-flex">
    <li><a href="#">About</a></li>
    <li><a href="#">サイトマップ</a></li>
    <li><a href="#">プライバシーポリシー</a></li>
  </ul>
  <p class="copyright">© 2023 Example Inc. All Rights Reserved.</p>
</footer>
```
### 🎨 CSS
```css
html {
  font-family: sans-serif;
}

body {
  background: #333;
}

a {
  color: #999;
  text-decoration: none;
}

ul {
  list-style: none;
  padding: 0;
}

.footer {
  padding: 2rem;
  font-size: 15px;
  color: #999;
  background: #fff;
  border-top: 1px solid #e5e7eb;
}

.footer a:hover {
  color: #000;
}

@media (min-width: 768px) {
  .footer {
    display: flex;
    justify-content: space-between;
  }

  .md-flex {
    display: flex;
  }

  .md-flex li + li {
    margin-left: 16px;
  }
}
```

---
## 🪞 ロゴありフッターテンプレート

フッターには、ブランドロゴやサイトロゴを入れるケースが多いですよね。  
以下は **ロゴ付きのfooter構成** です。  
ロゴ・ナビ・コピーライトがシンプルにまとまり、どんなサイトにも合わせやすいデザインです。

---

### 💻 HTML

```html
<footer class="footer">
  <div class="md-flex md-justify-between">
    <a href="https://jajaaan.co.jp/" class="footer__logo">
      <img
        src="https://jajaaan.co.jp/wp-content/themes/jajaaan/assets/images/dist/svg/logo.svg"
        width="140"
        height="20"
        alt="JAJAAAN Logo"
      />
    </a>
    <ul class="footer__navi flex">
      <li><a href="#">About</a></li>
      <li><a href="#">サイトマップ</a></li>
      <li><a href="#">プライバシーポリシー</a></li>
    </ul>
  </div>
  <hr />
  <p class="copyright">
    © 2023 <a href="https://jajaaan.co.jp/">JAJAAAN Inc.</a> All Rights Reserved.
  </p>
</footer>
```
🎨 CSS
```css
html {
  font-family: sans-serif;
}

body {
  background: #333;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

a {
  color: #999;
  text-decoration: none;
}

a:hover {
  color: #000;
}

.flex {
  display: flex;
}

hr {
  height: 1px;
  border: 0;
  border-top: 1px solid #e5e7eb;
}

.footer {
  padding: 2rem;
  font-size: 15px;
  color: #999;
  background: #fff;
}

.footer__navi {
  flex-wrap: wrap;
  margin-bottom: 2rem;
}

.footer__navi li {
  display: inline-block;
}

.footer__navi li:not(:last-child) {
  margin-right: 16px;
}

.footer__logo {
  display: inline-block;
  margin-bottom: 1rem;
}

@media (min-width: 768px) {
  .md-flex {
    display: flex;
  }

  .md-justify-between {
    justify-content: space-between;
  }

  .copyright {
    text-align: left;
  }
}

```

---
## 🪞 情報を増やしたフッター

よく見る形のfooterですね。

---

### 💻 HTML

```html
<footer class="footer">
  <div class="md-flex md-justify-between">
    <a href="https://jajaaan.co.jp/" class="footer__logo">
      <img src="https://jajaaan.co.jp/wp-content/themes/jajaaan/assets/images/dist/svg/logo.svg" width="140" height="20" alt="JAJAAAN Logo" />
    </a>
    <div class="grid">
      <div>
        <p class="footer__navi-heading">SERVICE</p>
        <ul class="footer__navi">
          <li><a href="#">サービスA</a></li>
          <li><a href="#">サービスB</a></li>
          <li><a href="#">サービスC</a></li>
        </ul>
      </div>
      <div>
        <p class="footer__navi-heading">FOLLOW US</p>
        <ul class="footer__navi">
          <li><a href="#">Facebook</a></li>
          <li><a href="#">Twitter</a></li>
          <li><a href="#">Instagram</a></li>
        </ul>
      </div>
      <div>
        <p class="footer__navi-heading">ABOUT</p>
        <ul class="footer__navi">
          <li><a href="#">会社概要</a></li>
          <li><a href="#">お問い合わせ</a></li>
          <li><a href="#">サイトマップ</a></li>
          <li><a href="#">プライバシーポリシー</a></li>
        </ul>
      </div>
    </div>
  </div>
  <hr />
  <p class="copyright">© 2023 <a href="https://jajaaan.co.jp/">JAJAAAN Inc.</a> All Rights Reserved.
  </p>
</footer>
```

🎨 CSS
```css

html {
  font-family: sans-serif;
}

body {
  background: #333;
}

ul {
  padding: 0;
  list-style: none;
}

a {
  color: #4b5564;
  text-decoration: none;
}

a:hover {
  color: #000;
}

hr {
  height: 1px;
  border: 0;
  border-top: 1px solid #e5e7eb;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.footer {
  padding: 2rem;
  font-size: 15px;
  color: #4b5564;
  background: #fff;
}

.footer__navi-heading {
  font-weight: 600;
}

.footer__logo {
  display: inline-block;
  margin-bottom: 2rem;
}

.footer__navi li {
  margin-bottom: 0.75rem;
}

@media (min-width: 768px) {
  .md-flex {
    display: flex;
  }

  .md-justify-between {
    justify-content: space-between;
  }

  .grid {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
}
```

---
## 🪞 連絡先要素追加したパターン

連絡先を追加したパターンのfooterです。  
連絡先などの情報はaddressタグで囲みます。  
住所などが長い場合は、閲覧サイズによって改行される場合があるので注意します。  
電話番号などを設置する場合はスマホでタップできることが分かるように色を変えたり、下線を入れるといいかもしれません。  
PCなどのデバイスではこのリンク機能はいらないので、下線を消したり、pointer-events: none;でクリックができないようにします。

---

### 💻 HTML

```html
<footer class="footer">
  <div class="lg-flex md-justify-between">
    <div>
      <a href="https://jajaaan.co.jp/" class="footer__logo">
        <img src="https://jajaaan.co.jp/wp-content/themes/jajaaan/assets/images/dist/svg/logo.svg" width="140" height="20" alt="JAJAAAN Logo" />
      </a>
      <address class="footer__address">
        株式会社Company<br />
        〒163-8001 東京都新宿区西新宿２丁目８−１<br />
        TEL：<a href="tel:">0120-123-456</a> / FAX：0120-123-456<br />
      </address>
    </div>
    <div class="grid">
      <div>
        <p class="footer__navi-heading">SERVICE</p>
        <ul class="footer__navi">
          <li><a href="#">サービスA</a></li>
          <li><a href="#">サービスB</a></li>
          <li><a href="#">サービスC</a></li>
        </ul>
      </div>
      <div>
        <p class="footer__navi-heading">FOLLOW US</p>
        <ul class="footer__navi">
          <li><a href="#">Facebook</a></li>
          <li><a href="#">Twitter</a></li>
          <li><a href="#">Instagram</a></li>
        </ul>
      </div>
      <div>
        <p class="footer__navi-heading">ABOUT</p>
        <ul class="footer__navi">
          <li><a href="#">会社概要</a></li>
          <li><a href="#">お問い合わせ</a></li>
          <li><a href="#">サイトマップ</a></li>
          <li><a href="#">プライバシーポリシー</a></li>
        </ul>
      </div>
    </div>
  </div>
  <hr />
  <p class="copyright">© 2023 <a href="https://jajaaan.co.jp/">JAJAAAN Inc.</a> All Rights Reserved.
  </p>
</footer>

```

🎨 CSS
```css
html {
  font-family: sans-serif;
}

body {
  background: #333;
}

ul {
  padding: 0;
  list-style: none;
}

a {
  color: #4b5564;
  text-decoration: none;
}

a:hover {
  color: #000;
}

hr {
  height: 1px;
  border: 0;
  border-top: 1px solid #e5e7eb;
}

address {
  font-style: normal;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.25rem;
  margin-bottom: 1.5rem;
}

.footer {
  padding: 2rem;
  font-size: 15px;
  color: #4b5564;
  background: #fff;
}

.footer__navi-heading {
  font-weight: 600;
}

.footer__logo {
  display: inline-block;
  margin-bottom: 1.5rem;
}

.footer__navi li {
  margin-bottom: 0.75rem;
}

.footer__address {
  margin-bottom: 2rem;
}

.footer__address a {
  text-decoration: underline;
}

@media (min-width: 768px) {
  .md-flex {
    display: flex;
  }

  .md-justify-between {
    justify-content: space-between;
  }

  .grid {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
  
  .footer__address a {
    text-decoration: none;
    pointer-events: none;
  }
}

@media (min-width: 1024px) {
  .lg-flex {
    display: flex;
  }
}

```

