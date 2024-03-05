# Spring Framework

## WAS

## WS

## CORS

## Servlet

## Dispatcher Servlet

### HandlerMapping

### HandlerAdapter

### ViewResolver

## MVC

## Spring AOP

    *. must have Interface
    1. Dynamic Proxy
    2. Pointcut
    3. Advice
    4. ~ doSomething

## AspectJ AOP

    *. do not use Proxy
    1. Make byteCode
    2. Find target
    3. Weaving
        3-1. When Compile
        3-2. When Class file load to JVM

## ThreadLocal

    1. 스프링 MVC 방식은 Multi Thread 기반으로 동작하는 웹 프레임워크다.
    2. Thread Pool 만들어서 요청이 들어오면 꺼내서 사용한 뒤 반환한다.
    3. ThreadLocal 개념은 각 쓰레드에 할당되는 저장공간을 뜻한다.
    4. 따라서 Multi Thread 환경에서는 Thread를 재사용하므로 ThreadLocal 공간에 값을 저장하면 반드시 초기화해야한다.

## Spring WebFlux

    1. Spring MVC 방식은 Blocking + 동기 방식으로 작동한다.
    2. 해당 방식은 응답성이 떨어지므로, 비동기적 요청을 처리하기 위한 방법이 필요해짐.
    3. Reactive Programming 개념을 기반으로 비동기 데이터 스트림을 사용하여 Non-Blocking 앱을 개발하기 위한 도구가 등장한다.
    4. Spring WebFlux

## Content Delivery Network

    1. 물리적으로 멀리 떨어진 사용자에게 컨텐츠를 보다 빠르게 제공하기 위해 고안된 기술.
    2. 사용자에게 가까운 곳에 서버를 만들고 데이터를 캐싱하여 보다 가까운 서버에서 컨텐츠를 내려받을 수 있게 함.
    3. 가까운 서버에 데이터가 없다면, 가장 근접한 버전의 캐싱된 데이터를 제공한다.
    4. 컨텐츠 자체를 찾을 수 없다면 CDN 내부 다른 서버에 컨텐츠를 요청하여 찾은 후 사용자에게 응답한다.

## DI

## DL

## IoC

## AOP

## VO

## DAO

## BO, Service

## DTO

## VO

