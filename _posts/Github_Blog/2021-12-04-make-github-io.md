---
title: "[github.io] jekyll 시작하기"
categories:
    - Github_Blog
tags:
    - Jekyll
    - Blog
---

## 환경 설정
### 1. Ruby
jekyll을 사용하기 위해서는 ruby가 필요하다.
[rubyinstaller](https://rubyinstaller.org/downloads/)에서 WITH DEVKIT 중 (x86)으로 다운받아 설치해준다.
> **jekyll**이 32bit이므로 **(x86)**을 설치해줘야 한다.

![rubyinstaller](https://images.velog.io/images/kimsoyeong/post/5cf03a76-8907-4fff-a2da-0eae7efd0d96/image.png)

나는 Ruby+Devkit 2.7.5-1 (x86) 버전으로 모든 설정 default로 설치했다.
설치가 끝나면, ridk install 선택해제 후 완료한다.

### 2. jekyll
시작에서 Start Command Prompt with Ruby을 실행한다.

![Start Command Prompt with Ruby](https://images.velog.io/images/kimsoyeong/post/6d6345c8-3300-4ac5-8a50-19596d41452f/image.png)

cmd에 아래 명령어를 실행한다.

```bash
gem install jekyll
```

`ruby -v` 와 `jekyll -v`로 정상적으로 설치되었음을 확인한다.


## minimal-mistakes 테마 적용
- [minimal-mistakes github](https://github.com/mmistakes/minimal-mistakes)

minimal-mistakes 리포지토리를 clone해준다.
.github, test, .editorconfig, .gitattributes, .travis.yml, CHANGELOG.md, README.md, screenshot.png, screenshot-layouts.png는 필요없으므로 삭제한다.

docs/_pages를 root 디렉토리로 이동시킨다. _pages 내부에서 404.md, about.md, category-archive.md, home.md, page-a.md, page-archive.html, page-b.md, tag-archive.md 만 남겨둔다. (아직까지는 이 외의 파일들의 쓸모를 찾지 못함)

### 로컬 서버에서 실행
github에 바로 push를 하게 되면 잘못된 커밋도 모두 로그가 남고 번거롭다.
push 전에 로컬에서 정상 작동을 확인하자!

ruby prompt에 다음 명령을 실행한다.

```
gem install bundler
bundler exec jekyll serve
```

사실 나는 `jekyll serve` 이전에 아래 명령도 실행해줬다. jekyll은 여러 gem들에 의존한다. bundle install을 통해 테마에 필요한 것들을 설치해줄 수 있다.

```
bundle install
bundle update
```

[http:/127.0.0.1:4000](http:/127.0.0.1:4000) 에서 블로그 실행을 확인할 수 있다.


## Github.io Repo 생성
repository name을 `github_id`.github.io로하여 repostiory를 만든다.

![github.io repository](https://images.velog.io/images/kimsoyeong/post/c63295f1-fefa-436b-8556-66588099c159/image.png)

minimal-mistakes 테마 적용에서 만들어둔 모든 파일을 해당 repo에 push한다.

![gihub.io](https://images.velog.io/images/kimsoyeong/post/de1ecd45-e918-4d1d-a5f7-d12e47cd9c35/image.png)

`github_id.github.io` 에서 블로그를 확인할 수 있다.