# 데이터베이스 

##  1. DDL,DML,DCL

     1. DDL - Data Definition Language 데이터 정의 언어
        - Create Drop Alter Truncate
     2. DML - Data Manipulation Language 데이터 조작 언어
        - Select Update Delete Insert
     3. DCL - Data Control Language 데이터 컨트롤 언어
        - Grant Revoke

    - 데이터베이스의 무결성 제약조건
        1) 개체 무결성 : DB안에 있는 Primary Key는 Null값을 가져서는 안된다.
        2) 참조 무결성 : 한 개체가 Foreign Key를 가지고 있을때 그 Foreign Key는 참조할 수 없는 값을 가져서는 안된다.
        3) 고유 무결성 : Unique 속성을 갖게된 경우 중복을 허락해서는 안된다.
        4) 도메인 무결성 : 속성에 정의된 값만 데이터로 가져야 한다.
        5) Null 무결성 : attribute가 Null값을 가져서는 안된다.

##  2. 데이터베이스의 정규화

    1) 정규화의 목적 
        - 데이터베이스의 변경시 이상 현상 제거

    제 1정규화 - 원자형 도메인으로 스키마 내부에 있는 모든 Attribute가 더이상 나눌 수 없는 상태일때 제 1정규형을 만족한다고 한다.

    제 2정규화 - 기본키가 2개 이상의 속성으로 이루어진 경우, 부분 함수 종속성 제거

    제 3정규화 - 이행 함수 종속성 제거

    Boyce Code Normal Form (보이스 코드 노말 폼 , 가장 이상적인 상태) - 결 
    
    제 4정규화 - 다   

    제 5정규화 - 조   


##  3. 데이터베이스의 질의처리

##  4. 데이터베이스의 트랜잭션

    1) 트랜잭션의 성질 
        - 원자성(Atomicity) : 트랜잭션의 내용을 모두 반영하거나 아예 반영하지 말아야 한다. (문제 생기면 취소해야됨)
        - 독립성(Isolation) : 하나의 트랜잭션이 실행되는 동안 다른 트랜잭션에 영향을 끼쳐서는 안된다.
        - 일관성(consistency) : 트랜잭션 수행 전과 트랜잭션 수행 완료 후의 상태가 같아야 한다.
        - 영속성(persistency) : 영구적으로 반영되어야 한다.

##  5. 데이터베이스의 동시성 제어
