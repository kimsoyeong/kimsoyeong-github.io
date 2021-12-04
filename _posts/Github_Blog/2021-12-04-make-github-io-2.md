---
title: "[github.io] _config.yml 설정하기"
categories:
    - Github_Blog
tags:
    - Blog
---

minimal-mistakes repo를 clone했기 때문에 이미 **_config.yml** 파일이 root 경로에 존재할 것이다. 해당 파일을 수정하여 <U>블로그 설정을 커스텀해보자!</U>

## Site Settings

사이트(블로그) 기본 설정이다.

```yml
minimal_mistakes_skin    : "dirt" # "defautl", "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"

# Site Settings
locale                   : "ko-KR"          # 블로그 언어
title                    : "Soyang.log"     # 블로그 이름
title_separator          : "-"
subtitle                 : # site tagline that appears below site title in masthead
name                     : "soyang"         # 블로그에서 사용될 닉네임
description              : "해보지 않고는 당신이 무엇을 해낼 수 있는 지 알 수가 없다. ✨"      # 블로그 설명: 블로그 링크 공유 시 표시
url                      : "https://kimsoyeong.github.io"                                   # 블로그 url
baseurl                  : # the subpath of your site, e.g. "/blog"
repository               : "https://github.com/kimsoyeong/kimsoyeong.github.io"             # Github repo url
teaser                   : # path of fallback teaser image, e.g. "/assets/images/500x300.png"
logo                     : # path of logo image to display in the masthead, e.g. "/assets/images/88x88.png"
masthead_title           : # overrides the website title displayed in the masthead, use " " for no title
```

## Site Author

사용자 프로필 설정이다.

```yml
author:
  name             : "soyang"   # 이름
  avatar           : "/assets/images/bio-photo.jpg"   # 프로필 사진
  bio              : "💻 keep studying 📜"  # biography
  location         : "Korea"    # 지역
  email            :            # links에서 작성
  links:
    - label: "Email"
      icon: "fas fa-fw fa-envelope-square"
      url: mailto:soyeong.kim9@email.com
    - label: "Website"
      icon: "fas fa-fw fa-link"
      url: "https://soso-cod3v.tistory.com/"
    # - label: "Twitter"
    #   icon: "fab fa-fw fa-twitter-square"
      # url: "https://twitter.com/"
    # - label: "Facebook"
    #   icon: "fab fa-fw fa-facebook-square"
      # url: "https://facebook.com/"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/kimsoyeong"
    # - label: "Instagram"
    #   icon: "fab fa-fw fa-instagram"
      # url: "https://instagram.com/"
```

## Site Footer

하단 footer 설정이다.

```yml
footer:
  links:
    - label: ""
      icon: "fas fa-fw fa-envelope-square"
      url: mailto:soyeong.kim9@email.com
    # - label: "Twitter"
    #   icon: "fab fa-fw fa-twitter-square"
      # url:
    # - label: "Facebook"
    #   icon: "fab fa-fw fa-facebook-square"
      # url:
    - label: ""
      icon: "fab fa-fw fa-github"
      url: "https://github.com/kimsoyeong"
    # - label: "GitLab"
    #   icon: "fab fa-fw fa-gitlab"
      # url:
    # - label: "Bitbucket"
    #   icon: "fab fa-fw fa-bitbucket"
      # url:
    - label: ""
      icon: "fab fa-fw fa-instagram"
      url: "https://www.instagram.com/yeong._.99/"
```

## Outputting

홈 화면에서 노출되는 게시글(post) 개수를 설정한다.

```yml
# Outputting
permalink: /:categories/:title/
paginate: 6 # amount of posts to show   # defaults: 5
paginate_path: /page:num/
timezone: # https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
```


## Defaults

```yml
# Defaults
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: # true
      share: true
      related: true

  # _pages                  : 아래를 새로 추가
  - scope:
      path: "_pages"
      type: pages
    values:
      layout: single
      author_profile: true
```

이렇게 사이트 설정이 끝났다.

다음에는 게시글(post)의 카테고리를 설정하는 법을 정리해볼 것이다.