# 실습 1) 거래액 데이터 분석

-2017년부터 2021년 3월까지의 전자상거래 추정거래액 (단위 : 백만원)

-내 회사의 거래액 데이터라고 생각해도 됨 (만약 내 회사가 다양한 상품군을 취급하는 유통업체라면 각 상품별 매출액이 어떻게 변화했는가의 관점)



--1) 데이터 탐색--------------------------------------------------------------



--STEP 1) 모든 컬럼 추출하기 ( = 이 데이터가 어떻게 생겼는지를 확인 )

**select** *

**from** gmv_trend

*# gmv_trend 라는 Table로 부터 데이터를 뽑을 것이므로 table 명 앞에 from을 쓰기*

*#한 줄 올라가서 selcet.*

즉, 이 table로 부터 무엇인가를 선택할 것이라는 뜻이며, 별표는 모든 칼럼이라는 의미이므로 모든 칼럼을 선택하겠다는 걸 나타냄.

*#실행은 ctrl+enter*



--STEP 2) 특정 컬럼 추출하기

**select** category, yyyy ,mm, gmv 

**from** gmv_trend



--STEP 3) 중복값 없이 특정 컬럼 추출하기

**select distinct** category

**from** gmv_trend

*#category의 중복값들이 사라짐.*



**select** **distinct** yyyy, mm

**from** gmv_trend

*#년, 월 전체의 중복값 사라짐 (2017. 01~2021.03까지 표시)*



--2) 특정 연도의 매출 탐색--------------------------------------------------------------



--2-1) 조건이 하나일 때 More Example

------a) 숫자열 (between, 대소비교)



------b) 문자열 (=, !=, like, in, not in)



--2-2) 조건이 여러개일 때--------------------------------------------------------------

------a) and 조건







--3) 카테고리별 매출 분석--------------------------------------------------------------



--More Example) 카테고리별, 연도별 매출



--More Example) 전체 총합



--More Example) 집계함수의 종류



--group by + where 예시







--4)매출이 높은 주요 카테고리만 확인하기--------------------------------------------------------------





--More Example) where절이랑 같이 쓰기







--5) 매출이 높은 순으로 카테고리 정렬하기--------------------------------------------------------------



--내림차순 Example



--[추가 예제 1] 복수의 컬럼으로 정렬



--[추가 예제 2] select 절에 없는 컬럼으로 정렬 가능할까? -> 불가능
