---
title: 커밋 하면 코드에 prettier 적용하기
layout: post
date: '2021-01-21 19:00:00'
categories:
  - pre-commit hook
  - sourcetree
---

## Git Hook

훅은 커밋할 때 가장 먼저 호출되는 훅으로 커밋 메시지를 작성하기 전에 호출된다.

## Install Prettier

```bash
~/vantamin $ yarn add --dev --exact prettier
~/vantamin $ echo {}> .prettierrc
```

## Pre-commit Hook

Install husky, lint-staged

```bash
~/vantamin $ npx mrm lint-staged
```

package.json

```json
{
  "lint-staged": {
    "**/*": "prettier --write --ignore-unknown"
  }
}
```

## 문제점 및 해결 방법

맥에서 *Sourcetree.app*을 사용하여 커밋 하면 동작하지 않는다.

터미널에서 다음 명령어로 *Sourcetree.app*을 실행하면 해결할 수 있다.

```bash
$ open /Applications/Sourcetree.app
```

## 북마크

- [Prettier Options](https://prettier.io/docs/en/options.html)
- [Pre-commit Hook](https://prettier.io/docs/en/precommit.html)
- [Git Hooks](https://git-scm.com/book/ko/v2/Git%EB%A7%9E%EC%B6%A4-Git-Hooks)
