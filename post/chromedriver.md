---
title: chromedriver
date: 2024-06-16 17:40:43 +0900
draft: false
summary: "installing chromedriver"
---
# chromedriver 버전 문제
1. chromedriver 버전을 너무 낮은 걸 설치하면, 최신형 chrome을 사용할 줄 몰라서 실행이 안 된다.
2. 한편 chrome은 최신형 말고는 찾을 수가 없다.
3. 아래와 같이 행동하자.

# selenium 스크랩 위해 chromedriver 설치 
0. https://bill1224.tistory.com/381 를 참고.
1. 위 링크대로 linux용 chrome을 설치한다.
2. https://googlechromelabs.github.io/chrome-for-testing/ 에서 버전을 찾아 
{{< highlight shell >}}
sudo wget https://chromedriver.storage.googleapis.com/(버전명)/chromedriver-linux64.zip
{{< / highlight >}}
를 한다.
3. 이후
{{< highlight shell >}}
sudo unzip chromedriver-linux64.zip
sudo mv chromedriver /bin/chromedriver
which chromedriver
{{< / highlight >}}
를 한다.

4. 이후는 블로그 그대로 
