---
title: "HTMLInputElement: disabled プロパティ"
slug: Web/API/HTMLInputElement/disabled
l10n:
  sourceCommit: a36633398f827c87eb593f9647ed00bf33fd5b34
---

{{ APIRef("HTML DOM") }}

**`HTMLInputElement.disabled`** は [`disabled`](/ja/docs/Web/HTML/Element/input#disabled) という HTML の属性を反映した論理値で、このコントロールが無効であるかどうかを表します。無効である場合、クリックを受け付けません。無効化された要素は使用できず、クリックもできません。

## 値

論理値です。

## 例

### HTML

```html
<p>
  <label>
    <input id="check-box" name="b" value="1" type="checkbox" disabled /> このボックスをチェックしてください。
  </label>
</p>
<p>
  <label>
    <input id="toggle-box" name="b" value="2" type="checkbox" /> 他のボックスを有効にします。
  </label>
</p>
```

### JavaScript

```js
const checkBox = document.getElementById("check-box");
const toggleBox = document.getElementById("toggle-box");

toggleBox.addEventListener(
  "change",
  (event) => {
    checkBox.disabled = !event.target.checked;
  },
  false
);
```

### 結果

{{EmbedLiveSample('Examples')}}

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}
