---
title: 브라우저 동작 방식
layout: post
date: '2021-02-18 19:00:00'
---

처음 브라우저 동작 과정을 보았을 때 무언가 복잡해 보였다.

과정이 순서대로 이뤄지지 않아 보였고 이리저리 얽혀 보였다. 하지만 결국엔 브라우저는 동기적으로 (순서대로) 동작한다는 것으로 이해했고 내가 작성한 코드들이 어떠한 과정을 통해 브라우저에서 그려지는지 나 나름대로 직관적으로 이해해 보았다.

![WebKit main flow](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/webkitflow.png)

> WebKit main flow (이미지 출처 : 북마크 참고)

사용자가 브라우저 주소창에 웹페이지 주소를 입력해 웹페이지를 요청하고 서버는 요청받은 웹페이지를 전송한다. 그러면 브라우저는 HTML을 로드(Load)한다.

로드된 HTML 문서를 브라우저 렌더링 엔진에서 파싱(Parsing)을 진행하고 HTML 문서에 CSS나 JavaScript 파일을 요청하고 있으면 서버로부터 해당 파일들 로드한다.

로드된 CSS 역시 렌더링 엔진에서 파싱 되고 HTML은 DOM(Document Object Model) tree, CSS는 CSSOM(CSS Object Model) tree를 생성한다.

로드된 JavaScript는 자바스크립트 엔진을 통해 파싱 되어 Syntax tree를 생성한다. HTML 문서를 파싱 하는 과정에서 script 태그를 만나면 자바스크립트 엔진에서 해당 과정을 동적으로 실행하고 실행이 완료되면 다시 HTML 파싱을 이어서 진행한다.

브라우저 렌더링 엔진에서 DOM과 CSSOM을 생성했으면 이를 결합하여 Render tree를 생성한다.

Render tree가 생성됐다면 브라우저에서 웹페이지를 보여주게 된다.

WebKit 브라우저 엔진을 기초로 했지만 Mozilla의 Gecko 브라우저 엔진도 비슷하거나 거의 동일한 과정으로 진행된다.

## 북마크

- [How Browsers Work: Behind the scenes of modern web browsers](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
- [브라우저는 어떻게 동작하는가?](https://d2.naver.com/helloworld/59361)
