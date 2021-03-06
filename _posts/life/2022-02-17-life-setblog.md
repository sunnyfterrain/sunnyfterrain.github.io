---
layout: post
title: '[개발] Github 블로그 세팅이 완료! Velog 에서 옮긴 이유?'
subtitle: '[개발] Github 블로그 세팅이 완료! Velog 에서 옮긴 이유?'
category: life
tags: life
---
[테마]:http://jekyllthemes.org/
[velog]:https://velog.io/
[hydejack]:https://hydejack.com/

<!-- more -->

1. this ordered seed list will be replaced by the toc 
{:toc}

## 들어가기에 앞서
---
개발 관련 지식을 얻기 위해 여러 개발자분들의 블로그들을 돌아다니다 보면  
티스토리, 벨로그 등이 아닌 흔히 말하는 깃헙 블로그이신 분들이 많이 보였다.

나도 당시에는 개발 블로그로 [Velog]를 시작했지만 서비스하고 있는 블로그가 아닌  
나만의 블로그가 가지고 싶었고, 꼭 만들자고 다짐했다.

그렇게 다짐만 한지 한 달 뒤.. 드디어 세팅이 끝났다.
<br>

## 왜 Jekyll 인가?
---
흔히 구글에서 깃헙 블로그를 검색하면 Jekyll(지킬) 블로그가 많이 나온다.  
지킬 블로그는 깃헙 블로그를 만들 수 있는 정적 제네레이터 인데 Ruby로 만들어져있다.

다른 언어로 만들어진 것도 있지만 굳이 지킬로 한 데에는 그만큼 자료와 정보가 많기 때문이다.  
그래서 구글링을 해보면 Jekyll 기반으로 하는 블로그의 [테마]들이 엄청 많다.  
<br>

![theme](/assets/img/life/2022-02-17-life/2022-02-17-theme.png){:.centered} 이것은 수많은 테마들 중 일부분일 뿐이다.  
{:.figcaption}  
<br>


그중에 내가 선택한 것은 [Hydejack]이다. 깔끔하고 각종 효과가 있는 게 마음에 들었다.  
깃헙 블로그의 가장 큰 장점은 커스텀하기 쉽다는 것? 테마를 가지고 이미 커스텀 해서  
예쁘게 만들어져있는 다른 블로그도 깃헙 fork를 통해 퍼올수 있다.  
그리고 반응형이다!  
<br>

## Velog ? 깃헙 블로그 ?
---
사실 처음엔 [Velog]도 나쁘지 않았다. 매우 깔끔하고 마크다운은 당연히 지원하고 글쓰기도 편했다.  
하지만 내가 생각하기에 벨로그의 단점은 따로 메뉴가 없다는 것! Tag로만 의존하고 있다.  
<br>

![velog](/assets/img/life/2022-02-17-life/2022-02-17-velog.png){:.centered} 따로 메뉴 카테고리가 존재하지 않는다  
{:.figcaption}  
<br>
이것이 너무 불편했다ㅠㅠ 모아놓고 싶은 글이 있으면 관련 메뉴를 만들어 보관하고 싶은데  
그럴수가 없었고, 글이 많아지면서 같이 생기는 태그들은 나중되면 정말 지저분하게 많아진다.  

그에 반해 깃헙 블로그(jekyll)은 정말 내 마음대로 다 꾸밀수 있어서 좋다.  
내가 원하는 폰트, 내가 원하는 배경, 내가 원하는 메뉴구성 등 마음대로 할 수 있다.  

이것이 깃헙 블로그의 장점이고 단점이다.  

왜냐하면 글 하나를 쓰려면 글쓰기 버튼만 눌러서 되는게 아닌, 직접 내 컴퓨터에 블로그 파일이  
저장되어 있는 폴더에 가서 마크다운 파일 하나를 만들고 정해진 이름을 지정하여서 연결하고싶은  
메뉴와 카테고리, 태그 등 jekyll의 정해진 문법으로 다 직접 이어줘야한다.  

어느정도의 HTML, CSS, JavaScript의 이해도가 있어야 하는 것도 당연!  

그런데 이렇게 꾸미고 하는 게 귀찮고 성격에 안맞으면 서비스형 블로그로 가는 것이 옳다고 본다.  

깃헙블로는 위의 작업이 끝나도 끝이 아니다.  
로컬 서버로 미리 구동하고 내가 올린 포스팅이 잘 나오는지 일일이 확인 해 줘야한다.

모든 확인이 끝나면? 깃헙에 푸쉬한다. 그리고 페이지 빌드가 될때까지 기다린다.  
그래도 뿌듯함은 있다!! 나만의 블로그가 있다는 희소성과 함께!  
<br>  


![error](/assets/img/life/2022-02-17-life/2022-02-17-error.png){:.centered}이러한 빌드 실패가 계속 나오면 미쳐버린다!!
{:.figcaption}  

나도 처음에 세팅하는 것이 너무 힘들었다. 로컬에서 제대로 화면이 보여져도 깃헙에 올리면  
페이지 빌드가 실패하고ㅠㅠ 글 하나 올리는데 무슨 시간이 이렇게 오래 걸리는지..

## 마무리
---
세팅만 장장 일주일이 걸렸지만, 한번 하고나면 쉽고 지금은 나만의 블로그가 생겼다는 것에  
더욱더 애착이 가는거 가고 더 열심히 하게 되는거 같다.  

이제 미루지 말고 포스팅을 자주자주 하도록 힘써야겠다!  

평소에 깃헙 블로그, Jekyll에 관심 있었다면 구글 검색으로 정말 엄청나게 많은  
자료와 정보들이 많으니 한번 시도해 보는 것도 나쁘지 않다고 본다!
