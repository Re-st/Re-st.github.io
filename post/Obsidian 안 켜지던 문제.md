---
title: Obsidian 안 켜지던 문제
date: 2024-06-24 09:32:00 +0900
draft: false
summary: Obsidian 안 켜지던 문제
---
`*.mega` 파일이 약 1G 가량 있었음
다운로드에 애를 먹던 67개 파일이 이걸 뺑뺑이로 생성시켰음.
안켜지고 동기화에서 뺑뺑이 도는 게 며칠 된 문제인데 해결을 미뤘더니 종양처럼 곪아있는 상태임.

# 일단 `*.mega`를 다 지워 줌.
WSL로 `/mnt/c/Users/(유저명)/../(Vault)`에 가서,
```bash
find . -name "*.mega" -type f -print0 | xargs -0 rm -f
```
# 그리고 계속 다운만 받던 파일들도 지워 줌.
동기화에 애를 먹는 파일들은 upstream에서 update가 되었지만, 로컬에도 동명의 파일이 있으며 원인모를 충돌이 나는 상태임.
일단 local에서 지워 주기로 함 (조금 복잡한 결말을 낳았지만)
chatgpt로 파일 이름을 OCR해서, 
```bash
#!/bin/bash

files=(
"파일.md"
)

for file in "${files[@]}"
do
  find . -name "$file" -type f -print0 | xargs -0 rm -f
done
```
처럼 지움.

파일명이 너무 길면 중간에 *로 와일드카드 해주고, 
`$!.md`의 경우는 `\$\!.md`로 이스케이프 해줌.

# 마지막으로 지운 파일을 mega.nz에서 복구해줌
그렇게 삭제한 파일들은 upstream (웹사이트 그리고 최신 파일이 있던 컴퓨터)에서도 모두 날아갔을 것임.
mega.nz > 휴지통 > syncdebris > 오늘날짜 가서 모두 복구. (ctrl A로 모두 선택 > 오른쪽 마우스 > 복구)

이제 웹사이트에서 복구한 내용 (최신 내용임) 이 업스트림과 모든 컴퓨터에 들어갈 것임.
해결..!