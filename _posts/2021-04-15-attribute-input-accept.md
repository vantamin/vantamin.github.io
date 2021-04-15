---
title: <input type="file" /> 확장자 지정
layout: post
date: '2021-04-15 19:00:00'
categories:
  - html
  - input
  - accept
---

`<input type="file">` 태그에서 `accept` 속성으로 선택할 수 있는 확장자를 지정할 수 있다.

```html
<!-- file extension -->
<input type="file" accept=".gif,.jpg,.png,.doc" />

<!-- audio files -->
<input type="file" accept="audio/*" />

<!-- video files -->
<input type="file" accept="video/*" />

<!-- image files -->
<input type="file" accept="image/*" />

<!-- html files -->
<input type="file" accept="text/html" />

<!-- txt files -->
<input type="file" accept="text/plain" />

<!-- excel files -->
<input
  type="file"
  accept="application/vnd.ms-excel,application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
/>
```

## 북마크

- [HTML input accept Attribute](https://www.w3schools.com/tags/att_input_accept.asp)
- [Media Types](http://www.iana.org/assignments/media-types/media-types.xhtml)
