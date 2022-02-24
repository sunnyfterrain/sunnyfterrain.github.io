---
layout: post
title: '리액트(React) 에서 SCSS 사용하는 법'
subtitle: '리액트(React) 에서 SCSS 사용하는 법'
category: devlog
tags: tips react scss
---

프론트엔드 개발자라면 필수적으로 CSS 작업을 해야 할 일이 생긴다.  
그리고, React와 같은 라이브러리를 쓴다고해도 마찬가지이다.  

요즘은 많은 개발자들이 CSS 전처리기를 많이쓰고 있는데, 그중에 SCSS(SASS)와  
리액트를 연동하는 방법을 설명하고자 한다.  

<!-- more -->

1. this ordered seed list will be replaced by the toc 
{:toc}  

## 설치 방법  
---  

우선 터미널로 컴파일러를 설치해줘야 한다.  
* SCSS를 적용하고 싶은 리액트 앱 폴더로 이동한다.  
* 컴파일러를 설치한다.  
  * yarn 일 경우 `yarn add node-sass`  
  * npm 일 경우 `npm install node-sass`  

* 끝이다. 아주 간단하다.  

![json](/assets/img/tips/2020-02-23-react-scss/2022-02-23-react-scss.png){:.centered} package.json 파일  
{:.figcaption}  

* package.json 에 node-sass 가 있는지 확인하자!  

## 사용방법  
---  

사용방법은 CSS와 별반 다르지 않다. 원하는 폴더에 style.scss 파일을 만들고  
`import ./style.scss` 해주면 알아서 컴파일 해 준다.