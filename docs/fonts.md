# フォントの取得・設定方法

## 使用フォント

- **Inter** (Weight: 300, Subset: latin)

## 取得手順

1. [google webfonts helper](https://gwfh.mranftl.com/fonts/inter) にアクセス
2. 「Inter」を選択
3. Charsets: `latin` を選択
4. Styles: `300` を選択
5. Formats: `Modern Browsers`（woff2）を選択
6. フォントファイルをダウンロード
7. `public/fonts/` に配置

## 配置先

```
public/fonts/inter-v20-latin-300.woff2
```

## CSS

`public/css/style.css` の先頭に `@font-face` を記述。

```css
@font-face {
  font-display: swap;
  font-family: Inter;
  font-style: normal;
  font-weight: 300;
  src: url("../fonts/inter-v20-latin-300.woff2") format("woff2");
}
```
