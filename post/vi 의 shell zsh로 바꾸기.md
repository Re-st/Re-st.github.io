---
title: vi 의 shell zsh로 바꾸기
date: 2024-07-23 14:11:43 +0900
draft: false
summary: vi 의 shell zsh로 바꾸기
---
Vim에서 `!` 명령어를 사용하여 외부 명령을 실행할 수 있으며, 이를 통해 `zsh`에서 정의한 alias와 함수를 사용할 수 있다. 이를 위해서는 Vim에서 `zsh`를 쉘로 사용하도록 설정하면 된다. Vim이 기본적으로 사용하고 있는 쉘을 `zsh`로 변경하면 `zsh`의 환경설정을 그대로 사용할 수 있다.

Vim 설정 파일 (`~/.vimrc`)에 다음 줄을 추가한다.

```vim
set shell=/bin/zsh
```

이렇게 하면 Vim이 외부 명령어를 실행할 때 `zsh`를 사용하게 된다.