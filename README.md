# 반타코딩 블로그

반타코딩 블로그입니다.

## DEV 명령어 모음

### `git command`

```bash
$ git clone https://github.com/vantamin/vantamin.github.io.git vantamin
$ cd vantamin
~/vantamin $ bundle exec jekyll serve # => 브라우저로 http://localhost:4000 에 접속
~/vantamin $ git config --local user.name "vantamin"
~/vantamin $ git config --local user.email "vantablack.min@gmail.com"
~/vantamin $ git add --all
~/vantamin $ git commit -m "commit message"
~/vantamin $ git push -u origin master
```

### `yarn start`

```bash
~/vantamin $ yarn start # => bundle exec jekyll serve -l -o
```

## Sourcetree 실행

```bash
$ open /Applications/Sourcetree.app
```

## [환경설정 옵션](http://jekyllrb-ko.github.io/docs/configuration/options/) : [Configuration Options](https://jekyllrb.com/docs/configuration/options/)

| 설정        | 옵션과 플래그      |
| ----------- | ------------------ |
| Live Reload | `-l, --livereload` |
| Open URL    | `-o, --open-url`   |
