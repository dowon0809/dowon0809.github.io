---
layout: post
title:  "Spring Framework란?"
date:   2019-06-29 00:00:00 +0800
categories: default
tags: test
---
<span style="font-weight:bold; font-size:1.2rem;">Spring Framework</span>와 <span style="font-weight:bold; font-size:1.2rem;">MVC 패턴</span>의 이해

<br>

#### **Framework란?**
"프레임워크란, 소프트웨어의 구체적인 부분에 해당하는 설계와 구현을 재사용이 가능하게끔 일련의 협업화된 형태로 클래스들을 제공하는 것"<br>- 랄프 존슨(Ralph Johnson) -
<br>
<p style="font-size:1.4rem; font-weight:bold;">장점</p>
<span style="font-weight:bold; font-style:oblique;">첫째,</span> 개발 생산이 좋아진다.
<br>
Framework는 컴포넌트, 통신 및 데이터 처리 등 개발이 필요한 다양한 기능을 미리 제공하며, 백지상태에서 개발하는 방식에 비해 개발 생산성이 좋아진다.
<br><br>
<span style="font-weight:bold; font-style:oblique;">둘째,</span> 코드의 품질이 향상된다.
<br>
개발자가 반복적인 작업에서 실수하기 쉬운 부분들을 내부에서 처리하면서 버그 발생의 가능성을 최소화하여 코드의 품질이 향상된다.
<br><br>
<span style="font-weight:bold; font-style:oblique;">셋째,</span> 유지 보수가 안정적이고 편리하다.
비즈니스 환경이 빠르게 변화하면서 기업의 IT담당자들은 속도에 맞춰 지속적으로 시스템을 업데이트 해야만 한다. 이러한 상황에서 담당자가 바뀌는 상황이 생기면 유지보수의 문제와 마주하게 된다. Framework는 구조적으로 쳬게화된 개발 환경을 구축했다면 담당자가 변경되어도 그 패턴이 유사하기 때문에 위험을 최소화할 수 있으며 안정적인 시스템 운영 및 개발이 가능하다.
<br><br>
<p style="font-size:1.4rem; font-weight:bold;">단점</p>
<span style="font-weight:bold; font-style:oblique;">첫째,</span> 학습 시간이 필요하다.
<br>
Framework의 기본적인 사용법, 제공하는 기능들을 이해하고 습득하려면 학습에 어느 정도의 시간을 투자해야 한다.
<br><br>
<span style="font-weight:bold; font-style:oblique;">둘째,</span> 개발 자유도의 한계가 있다.
<br>
Framework를 기반으로 개발하다 보면, 구조와 패턴을 따라야하기 때문에 더 유연하게 개발하는 것에 제한적일 수 밖에 없다. Framework가 지원하지 않는 기능을 자체적으로 직접 구현할 필요가 있는데, 이 때 Framework로 인한 제약 사항이 발생할 수 있다. 
<br><br><br><br>

#### **Spring Framework란?**
Spring Framework는 Java Platform을 위한 오픈소스 애플리케이션 Framework로서 줄여서 Spring이라고 부른다. 동적인 웹 사이트를 개발하기 위한 여러가지 기능 및 서비스를 제공하고 있으며 공공기관의 웹 서비스 개발 시 사용을 권장하고 있는 전자정부 표준 프레임워크 기반 기술로서 쓰이고 있다.
<br>
<p style="font-size:1.4rem;">특징</p>
- <span style="font-size:1.1rem; font-weight: bold;">경량 컨테이너</span>로서 Java 객체 생성, 소멸과 같은 라이프 사이클을 관리하며 Spring으로 부터 필요한 객체를 얻어올 수 있다.
- <span style="font-size:1.1rem; font-weight: bold;">제어반전(IoC)</span>를 지원하여 컨트롤러의 제어권이 사용자가 아니라 Framework에 있어서 필요에 따라 Spring이 사용자의 코드를 호출한다.
- <span style="font-size:1.1rem; font-weight: bold;">의존성 주입(DI)</span>를 지원하여 각각의 계층이나 서비스들 간에 의존성이 존재할 경우 프레임워크가 서로 연결시켜 준다.
- <span style="font-size:1.1rem; font-weight: bold;">관점 지행 프로그래밍(AOP)</span>를 지원하여 트랜잭션이나 로깅, 보안과 같이 여러 모듈에서 공통적으로 사용하는 기능을 부니하여 관리한다.
- <span style="font-size:1.1rem; font-weight: bold;">영속성과 관련된 다양한 서비스</span>를 지원하여 iBatis나 Hibernate 등 이미 완성도가 높은 데이터베이스 처리 라이브러리와 연결할 수 있는 인터페이스를 제공한다.
- <span style="font-size:1.1rem; font-weight: bold;">확장성</span>이 높아 Spring Framework에 통합하기 위해 간단하게 기존 라이브러리를 감싸는 정도로 Spring에서 사용이 가능하기 때문에 수많은 라이브러리가 지원되고 있고 Spring에 사용되는 라이브러리를 별도로 분리하기도 용이하다.   

<br><br><br>

#### **MVC 패턴**
MVC 패턴이란 Model View Controller의 약자로서 데이터 구조를 나타내는 Model와 사용자에게 보여지는 화면인 View 그리고 Model과 View를 연결하는 Controller를 이용한 디자인 패턴이다. 
<br>
<p style="font-size:1.3rem; font-weight:bold;">DispatcherServlet</p>
Spring은 다른 웹 MVC Framework와 같이 Front Controller를 사용하며 여러 가지 기능을 제공하는 Servlet 중심으로 설계되어 있다. 이러한 Front Controller 역할을 수행하는 것이 DispatcherServlet이다. DispatcherServlet은 단순히 Front Controller 기능만 하는 것이 아니라 스프링 IoC 컨테이너와 통합되어 스프링의 모든 기능을 사용할 수 있게 한다. DispatcherServlet은 Spring MVC의 핵심요소이며 웹 요청의 Life Cycle을 주관한다.
- <span style="font-size:1.1rem; font-weight: bold;">Front Controller</span>는 모든 Web Application에 대한 요청들을 받고 그 요청을 Controller로 분배해준다.
- <span style="font-size:1.1rem; font-weight: bold;">Servlet</span>이란 클라이언트의 요청을 처리하고 그 결과를 다시 클라이언트에게 전송하는 Servlet 클래스의 구현 규칙을 지킨 Java 프로그램이다.
<br>
<p style="font-size:1.3rem; font-weight:bold;">Controller</p>
Controller란 클라이언트 요청이 진입하는 지점이며 요청에 따라 어떤 처리를 할지 결정해주며 클라이언트에게 View를 응답한다. Controller는 단지 요청을 결정만 해주며 실질적인 처리는 Service에서 담당한다. 규모가 커질수록 처리해야할 요청들이 많아지는데, 하나의 클래스에서 처리하는 것이 아닌 Controller라는 중간 제어자를 여러개 만들어 요청에 맞게 로직을 처리하도록 한다.
<br>
<p style="font-size:1.3rem; font-weight:bold;">Service</p>
클라이언트 요청에 필요한 정보를 제공하기 위한 처리를 담당한다. 하나 이상의 DAO를 통해 클라이언트의 요청에 맞게 데이터를 접근 또는 갱신하여 비즈니스 로직을 수행하고, 이를 하나 또는 여러개의 트랜잭션으로 묶는다. 즉, Service는 트랜잭션의 단위이다.
<br>
<p style="font-size:1.3rem; font-weight:bold;">DAO</p>
DAO는 Data Access Object의 약자로 말 그대로 DB의 데이터에 접근하는 객체이며, DB의 데이터를 읽거나 삽입 또는 삭제하는 데이터베이스 조작(DML)을 처리한다.
<br>
<p style="font-size:1.3rem; font-weight:bold;">DTO</p>
DTO는 Data Transfer object의 약자로 데이터 교환을 위한 Javabeans을 말하며, 별다른 로직이 없는 순수한 데이터 객체이다. 즉, Getter/Setter 메서드를 가진 객체를 의미한다.
<br><br><br>

##### Spring MVC Process
1. 클라이언트가 서버에 요청을 하면 DispatcherServlet가 클라이언트의 요청을 가로챈다.
2. 요청을 가로챈 DispatcherServlet은 HandlerMapping(URL 체크)을 통해 어떤 컨트롤러에게 요청을 위임할지 찾는다.
3. 매핑된 컨트롤러에서 @RequestMapping Annotation을 통해 요청을 처리할 메서드를 실행한다.
4. Controller에서 클라이언트의 요청을 처리할 Service를 주입(DI)받아 비즈니스 로직을 Service에게 위임한다.
5. Service에서 요청에 필요한 작업 대부분을 코딩하며, 데이터베이스 접근이 필요할 경우 DAO를 주입(DI)받아 DB 처리를 DAO에게 위임한다.
6. DAO는 MyBatis Framework를 이용해서 DB에 접근하여 CRUD를 통한 정보를 VO(DTO)에 담아 Service로 반환한다. 
7. Service는 모든 로직을 끝낸 결과를 Controller로 반환한다.
8. 결과를 받은 컨트롤러는 Model에 보여주고자 하는 View(JSP) 파일 정보와 결과 정보를 담아 DispatcherServlet으로 보낸다.
9. DispatcherServlet은 ViewResolver에게 받은 View 정보를 넘기며, ViewResolver는 응답할 View(JSP)를 찾아서 DispatcherServlet에게 알려준다.
10. DispatcherServlet은 응답할 View(JSP)에게 랜더링을 지시하고 View는 응답 로직을 처리한다.

<br><br><br>
<span style="font-size:1.2rem;">참고
	<br>
	<a href="http://tobetong.com/?p=6640">http://tobetong.com/?p=6640</a>
	<br>
	<a href="https://songsunbi.tistory.com/26">https://songsunbi.tistory.com/26</a>
</span>