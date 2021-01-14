---
title: 맥에서 Jekyll 블로그 설치하는 방법
layout: post
date: '2021-01-14 19:00:00'
---

## 필요 조건

```bash
$ ruby -v # 루비 2.4.0 이상
$ gem -v # 루비젬 설치 확인
$ gcc -v;g++ -v # GCC 설치 확인
$ make -v # Make 설치 확인
```

## Jekyll 시작하기

```bash
$ gem install jekyll bundler # jekyll, bundler 설치
$ jekyll new vantamin # jekyll 블로그 생성
$ cd vantamin # 디렉토리 이동
~/vantamin $ bundle exec jekyll serve # 로컬 서버 실행
```

## GitHub 배포하기

```bash
~/vantamin $ git init
~/vantamin $ git add --all
~/vantamin $ git commit -m "Initial commit"
~/vantamin $ git remote add origin https://github.com/vantamin/vantamin.github.io.git
~/vantamin $ git push -u origin master
```

## 북마크

- [Jekyll](http://jekyllrb-ko.github.io/)
