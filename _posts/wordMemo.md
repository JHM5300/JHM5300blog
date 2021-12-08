---
title: "ORM이란 무엇일까"
excerpt: "실무공부일지"
categories:
  - diary
toc: true
toc_sticky: true
tags:
  - 용어
  - 영어
---

# ORM 공부의 계기

일하면서 서버 작업환경에 대해서 들었다.
API작업을 시작하기전 얘기를 해주었지만, 그때 당신 이해하지 못하였다.
하지만 API작업을 만들면서 서버환경에 대해서 설명을 들으니 처음에 비하면 많이 이해가 되었다.
일하면서 모르고 당연하게 써왔지만
모르고 사용하는 것은 말도 안되는 것이라 생각하여

내가 사용하는 것이 무엇이며, 내가 사용하는 것 외 어떤 방법이 있는지
포스트를 작성을하며 이해를 도와야겠다.

ORM부터 작성을 해야겠다 ㅎㅎ!

## ORM(object-relational mapping란

- object reational mapping 객체 관계 매핑
  > 객체는 객체대로 설계하고, 관계형 데이터베이스는 관계형 데이터베이스대로 설계한다.
- ORM(object-relational mapping)은 객체와 RDB(Relational Database) 두 기둥위에 있는 기술이다.

## JPA(Java Persistence API) API란

- 자바 / 영속성 / API
- 자바 `ORM` 기술에 대한 표준 명세로 `JAVA`에서 제공하는 API이다.
- 자바 어플리케이션에서 관계형 데이터베이스를 사용하는 방식을 정의한 인터페이스이다.

  > JPA 인터페이스이다. 특정 기능을 하는 라이브러리가 아니다. 스프링의 `PSA`(Portable service Abstraction)에 의해서 표준 인터페이스를 정해두었는데, 그중 `ORM`(object-relational mapping)을 사용하기 위해 만든 인터페이스가 바로 JPA이다.

  ##### PSA

  > 하나의 추상화로 여러 서비스를 묶어둔 것을 Spring에서 `PSA`(Portable Service Abstraction)이라고 한다.
  > → https://sabarada.tistory.com/127

- ORM이기 때문에 자바 클래스와 DB테이블을 매핑한다(sql을 매핑하지 않는다.)

  ### ORM이 무엇일까 SQL Mapper 와 ORM

  - ORM은 DB테이블을 자바 객체로 매핑함으로써 객체간의 관계를 바탕으로 SQL을 자동으로 생성하지만 Mapper는 SQL을 명시해주어야한다.
  - ORM은 RDB(Relational Database)의 관계를 Object에 반영하는 것이 목적이라면, Mapper는 단순히 필드를 매핑시키는 것이 목적이라는 점에서 지향점의 차이가 있다.

  #### SQL Mapper

  - `SQL` ← mapping → `Object` 필드
  - `SQL` 문으로 직접 디비를 조작한다.
  - Mybatis, jdbcTemplate

  #### ORM(Object-Relation Mapping/ 객체-관계 매핑)

  - `DB 데이터` ← mapping → `Object` 필드
    - 객체를 통해 간접적으로 `DB 데이터`를 다룬다.
  - 객체와 디비의 데이터를 자동으로 매핑해준다.
    - SQL 쿼리가 아니라 메서드로 데이터를 조작할 수 있다.
    - 객체간 관계를 바탕으로 SQL을 자동으로 생성한다.
  - Persistant API라고 할 수 있다.
  - JPA, Hidernate

# 다음공부는

`@Synchronized`에 대해서
`@Transactional`(트랜젝셔널)에 대해서

# 단어 공부

`Relation` 관계
`Relational` 관계형
`Persistence` 지속성
`Persistant` 지속적
`Portable` 휴대용
`Abstraction`추상화
`영속성` 영원히 계속되는 성질이나 능력
