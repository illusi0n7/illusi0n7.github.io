---
layout: post
title: Github.io로 블로그 만들기
categories: [github]
tags: [jekyll, github, blog]
description: How to create personal blog using github
comments: true
---

git repository를 모아둔 `github`에서는 프로젝트 및 유저 사이트 생성을 지원한다. 다른 블로그 서비스와 다른점은 아얘 아무것도 없는 웹서버를 제공한다는 점이다. 웹서버를 제어할 수 있는 ssh같은 쉘을 열어주는건 아니지만, 저장소에 push 함으로써 웹서비스 관련 파일들을 올릴 수 있다. 

### github 가입
github에서 제공하는 서비스이므로 당연히 github 계정이 있어야한다. [**github**](https://github.com)에 가서 가입한다.  

### github.io 레파지토리 생성
git repository를 개인 웹서버로 활용하는 방식기때문에 저장소를 개설하여야한다. 이때 저장소의 이름은 반드시 **{github id}.github.io**로 생성하여야 하며, 이게 곧 블로그의 URL이다.

### jekyll 설치
jekyll은  Ruby로 작성된 정적 페이지를 쉽게 만들 수 있게 해주는 툴이다. github의 서버에서는 이미 동작하고 있기때문에 local에서 작업한 결과물을 보기위해서가 아니라면 따로 설치할 필요는 없다. [**여기**](https://github.com/barryclark/jekyll-now)에 있는 파일들을 모두 git repository에 올리면 기본적은 블로그의 틀이 잡힌다.  
가장 맘에 드는 기능은 마크다운으로 글을 작성하면 자동으로 html로 변환하여 보여준다는것이다.

### 테마 설치
[**jekyll 테마를 모아둔 사이트**](http://jekyllthemes.org/)가 있는데, 맘에드는 테마를 다운받고 바로위에 말한것처럼 repository에 통째로 올리면 해당 테마의 블로그가 생성된다.  
테마 각각에 적용되어있는 라이센스를 잘 확인하고 준수해야한다.

### 포스팅 하기
`jekyll 설치`나 `테마 설치`세션을 모두 마치고나면 **_posts**라는 폴더를 찾을 수 있는데, 그곳에 마크다운으로 포스팅 할 글을 작성하면 된다.   
글의 최상단에는 Jekyll에서 인식할수 있도록 제목, 태그, 카테고리, 설명 등 몇가지 설정을 작성해야한다. 다음은 이 글에대한 설정내용이다.
{% highlight yaml %}
layout: post
title: Github.io로 블로그 만들기
categories: [github]
tags: [jekyll, github, blog]
description: Test posting for check markdown.
comments: true
{% endhighlight %}
