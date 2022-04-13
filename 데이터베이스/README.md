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

##  2. 관계대수 연산자
    
    1. 필수 연산자 : Selection,Projection,Union,difference,Cartesian Product
    2. 유도된 연산자 : InterSection, SetaJoin,EqualJoin,Division
        -> Selection 과 Projection,Union,difference,Cartesian Product,Join 과 Division은 꼭 알아둬야함
##  3. 데이터베이스의 정규화

    1) 정규화의 목적 
        - 데이터베이스의 변경시 이상 현상 제거

    제 1정규화 - 원자형 도메인으로 스키마 내부에 있는 모든 Attribute가 더이상 나눌 수 없는 상태일때 제 1정규형을 만족한다고 한다. -> 한마디로 정리하자면 속성 값에 한개의 값만 들어가는게 1정규형이다.

    제 2정규화 - 기본키가 2개 이상의 속성으로 이루어진 경우, 부분 함수 종속성 제거

    제 3정규화 - 이행 함수 종속성 제거는 X->Y 이고 Y->Z 일 때 X->Z인 경우를 이행함수라고 한다. 이 부분을 제거해주는게 제 3정규화이다.

    Boyce Code Normal Form (보이스 코드 노말 폼 , 가장 이상적인 상태) - 결 
    
    제 4정규화 - 다   

    제 5정규화 - 조   

##  4. 데이터베이스의 개념,논리,물리 설계

    - 1. 개념적 설계 - 현실 세계에 맞춘 데이터베이스의 개념을 설계한다. 산출물로는 ER다이어그램이 있다.
    - 2. 논리적 설계 - ER 다이어그램을 바탕으로 서로 상호작용하는 논리를 설계한다. 논리 설계 단계에서 스키마를 작성한다. 정규화를 과정을 통해서 데이터베이스의 불필요한 부분을 제거해준다.
    - 3. 물리적 설계 - 개념 설계와 논리 설계를 바탕으로 테이블을 설계하고 , 반정규화를 통해서 데이터베이스를 최적화 한다.  


##  5. 데이터베이스의 트랜잭션

    1) 트랜잭션의 성질 
        - 원자성(Atomicity) : 트랜잭션의 내용을 모두 반영하거나 아예 반영하지 말아야 한다. (문제 생기면 취소해야됨)
        - 독립성(Isolation) : 하나의 트랜잭션이 실행되는 동안 다른 트랜잭션에 영향을 끼쳐서는 안된다.
        - 일관성(consistency) : 트랜잭션 수행 전과 트랜잭션 수행 완료 후의 상태가 같아야 한다.
        - 영속성(persistency) : 영구적으로 반영되어야 한다.



##  6. 데이터베이스의 동시성 제어

