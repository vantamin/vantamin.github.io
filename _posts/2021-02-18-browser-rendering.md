---
title: 브라우저 렌더링
layout: post
date: '2021-02-18 19:00:00'
categories:
  - browser
---

## 렌더링 엔진(Rendering Engine)

### 렌더링 엔진들

- 트라이던트 엔진(Trident Engine) : 인터넷 익스플로러(IE)
- 게코 엔진(Gecko Engine) : 파이어폭스(Firefox)
- [웹킷 엔진(Webkit Engine)](https://webkit.org/) : 사파리(Safari)
  - 블링크 엔진(Blink Engine) : 크롬(Chrome), 오페라(Opera)

### 동작 과정

1. DOM 트리 구축을 위한 HTML 파싱
   - HTML 문서 파싱, "콘텐츠 트리" 내부에서 태그를 DOM 노드로 변환
   - 외부 CSS 파일과 함께 스타일 요소 파싱(CSSOM 생성)
1. 렌터 트리 구축
   - DOM(Document Object Model)과 CSSOM(CSS Object Model)은 "렌더 트리" 생성
1. 렌더 트리 배치
1. 렌더 트리 그리기

## 파싱과 DOM 트리 구축

- 문서 파싱 : 브라우저가 코드를 이해하고 사용할 수 있는 구조로 변환하는 것
- 파싱 결과 : 문서 구조를 나타내는 노드 트리, 파싱 트리(parse tree) 또는 문법 트리(syntax tree)

## 북마크

- [How Browsers Work: Behind the scenes of modern web browsers](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
- [브라우저는 어떻게 동작하는가?](https://d2.naver.com/helloworld/59361)
