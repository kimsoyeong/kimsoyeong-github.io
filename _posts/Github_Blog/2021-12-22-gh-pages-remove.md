---
title: "Gihub Pages 비활성화"
categories:
    - Github
tags:
    - gh-pages
    - github
---

gh-pages를 사용해 배포중이던 사이트를 더이상 유지할 필요가 없어져 닫고자 한다.

## Gihub Pages 배포 중단하기

repository의 **gh-pages 브랜치를 제거**하면 간단히 해결된다.

branch를 제거 하기 위해서는 해당 프로젝트(repository)의 터미널에서 다음 명령어를 입력해야 한다.

```
git push origin --delete {branch_name}
```

gh-pages 브랜치를 제거해야 하므로 branch_name에 gh-pages를 입력해주면 된다! 

```
git push origin --delete gh-pages
```