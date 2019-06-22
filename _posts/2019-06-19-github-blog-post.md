---
layout: post
title:  "Github 블로그 만들기"
date:   2019-06-19 03:30:13 +0800
categories: default
tags: test
---
<span style="font-weight:bold; font-size:1.2rem;">Jekyll</span>과 <span style="font-weight:bold; font-size:1.2rem;">Github Pages</span>를 이용한 Github 블로그 생성 방법

<br>

#### **Jekyll란?**
Jekyll은 심플하고 블로그 지향적인 정적 웹 사이트 생성기이다. Jekyll은 Markdown, html 등의 파일을 템플릿 디렉토리로부터 읽어서 웹 서버에 바로 게시하여 정적 웹사이트를 만들 수 있다. 또한, Jekyll은 GitHub Pages의 내부 엔진이며 자신의 프로젝트 페이지나 블로그, 웹 사이트를 무료로 GitHub에 호스팅 할 수 있다.
*  **<a href="http://jekyllthemes.org" style="color:#222222; text-decoration: underline;">Jekyll 무료 테마 다운로드</a>**

<br>

#### **Github Pages란?**
Github Pages 는 Github 저장소의 내용을 웹페이지로 만들어 주는 서비스이며, Github 저장소의 내용을 직접 웹 페이지를 통해서 보여줄 수 있다. 즉, 무료로 웹 서버를 구축하여 자신의 블로그를 운영할 수 있다.
* **1개의 Github 계정으로 1개의 정적 웹 서버만 이용 가능**

<br>

#### **Github 블로그 만들기**
##### Github 저장소 만들기
<p style="font-size:1.1rem;">Github에 블로그용 저장소 만들기 <span style="color:blue; font-weight:bold;">("원하는 이름.github.io"와 같이 입력)</span></p>
<img src="{{site.url}}/assets/img/1_git_repo_make.png" style="width:100%;"/>

<br>

##### Jekyll 설치 및 테스트
<span style="font-size: 1.3rem; font-weight: bold;">Jekyll 설치</span>  
<p style="font-size: 1.1rem;">Jekyll은 하나의 Ruby 패키지이며 Jekyll을 설치하기 위해서 Ruby를 먼저 설치해야 한다. MacOS는 기본적으로 Ruby가 설치되어 있으며 아래의 명령어를 입력하여 Jekyll을 설치한다.</p>
{% highlight ruby %}
 $ sudo gem install jekyll bundler
{% endhighlight %}
<br>
<span style="font-size: 1.3rem; font-weight: bold;">Jekyll 테마 설정</span><br>
<p style="font-size: 1.1rem;"><a href="http://jekyllthemes.org" style="color:#222222; text-decoration: underline;">Jekyll 테마 사이트</a>에서 원하는 테마를 다운로드 한 뒤 "_config.yml" 파일에서 아래 항목의 값을 수정한다.</p>
{% highlight ruby %}
* title: "제목"
* baseurl: ""
* url: "Github 블로그 도메인" ex) https://dowon.github.io
* repository: "저장소 경로" ex) dowon0809/dowon.github.io
* user: "사용자 이름"
* user_email: "사용자 이메일"
{% endhighlight %}
<span style="color:red; font-weight: bold;">테마에 따라 설정해야 하는 값이 다를 수 있으며 위의 항목은 공통적인 부분을 추려낸 항목입니다.</span>  
<br>
<span style="font-size: 1.3rem; font-weight: bold;">Jekyll 로컬 테스트</span>  
<p style="font-size:1.1rem;">Jekyll 로컬 서버 구동을 위해 다운로드한 테마의 경로로 이동한 뒤 아래의 명령어를 순서대로 실행하여 bundle을 설치하고 Jekyll 로컬 서버를 구동한다.</p>
{% highlight ruby %}
 $ bundle install
 $ bundle exec jekyll serve
{% endhighlight %}

<br>

##### Github Pages에 배포하기
<span style="font-size:1.3rem; font-weight:bold;">Github 블로그 저장소 가져오기</span>
<p style="font-size:1.1rem;">Github 원격 저장소를 저장하고 싶은 경로로 이동한 뒤 아래의 명령어를 통해 원격 저장소를 PC로 가져온다.</p>
{% highlight ruby %}
 $ git clone "Github 저장소 웹 URL"
{% endhighlight %}
<p style="font-size:1.1rem;">설정한 테마의 모든 파일을 PC에 복제한 로컬 저장소에 복사한 후 아래의 명령어를 입력하여 Github 원격 저장소에 올린다.
{% highlight ruby %}
 $ git push -u origin master
{% endhighlight %}
<p style="font-size:1.1rem;">Push가 완료되면 5~10분 기다린 후 "https://설정한 이름.github.io"에 접속하여 확인한다.</p>
