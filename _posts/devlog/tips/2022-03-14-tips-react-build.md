---
layout: post
title: 'React build 후 빈화면만 나온다면?'
subtitle: 'React build 후 빈화면만 나온다면?'
category: devlog
tags: tips react
image:
  path:    /assets/img/reactlogo.png
---

리액트로 뚝딱뚝딱 무언가를 만들고 드디어 빌드!!  
`npm run build` ... 완료!! 얼른 Github에 올리고 배포배포! 자동배포 완료!  

엇.. 그런데.. 왜 빈화면만 나오지? 분명 빌드는 잘 됐는데..?

<!-- more -->

1. this ordered seed list will be replaced by the toc 
{:toc}  

## 설치방법  
---  

우선 터미널로 컴파일러를 설치해줘야 한다.  
* SCSS를 적용하고 싶은 리액트 앱 폴더로 이동한다.  
* 컴파일러를 설치한다.  
  * yarn 일 경우 `yarn add node-sass`  
  * npm 일 경우 `npm install node-sass`  

* 끝이다. 아주 간단하다.  
* 당연하겠지만 scss를 사용할 해당 리액트 앱 마다 따로 해줘야 한다.  

![json](/assets/img/tips/2022-02-23-react-scss/2022-02-23-react-scss.png){:.centered} package.json 파일  
{:.figcaption}  

* package.json 에 node-sass 가 있는지 확인하자!  

## 사용방법  
---  

* 지금까지 작업 하던 CSS의 확장자를 scss(sass) 로 변경  
  * 새로 작업 할 예정이라면 파일명.scss 으로 파일 생성
* 적용할 컴포넌트의 Import를 scss(sass) 로 변경 해준다.  
  * 예) `import "./App.scss"`
* 저장 하고 페이지 화면을 보면 아주 잘 적용되어 있는 것을 볼 수 있다!  