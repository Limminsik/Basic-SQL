# Basic-SQL
  HackerRank   https://www.hackerrank.com/domains/sql
  
  W3school     https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all
  
  ---
  
  
# 데이터 검색하기

> __* = 모든 것을 의미 ( 아스타 )__  
> -- : SQL 내에서 사용하는 주석

      SELECT *              -- SELCT 무엇을 선택
      FROM Customers        -- FROM 무슨 테이블로부터
      Limit 5;


## WHERE 절

      SELECT *
      FROM customers
      WHERE country = 'Germany'

## 비교 연산자 <, >

      SELECT *
      FROM customers
      WHERE customerID > 50

      SELECT *
      FROM customers
      WHERE customername < 'B'

## 논리 연산자 AND / OR
      SELECT *
      FROM CUSTOMERS
      WHERE customername < 'B' AND country = 'Germany'
      
      SELECT *
      FROM customers
      WHERE customername < 'B' OR country = 'Germany'


## LIKE,  IN,  BETWEEN,  IS NULL
 > % = 뒤에 어떤 것이 들어가도 상관 없다.
 > 
 > \ = 이스케이프 ;= 예약어를 탈출한다.  \ % = 예약어 %가 아닌 퍼센트 %를 의미  
 > 자신이 사용하는 DB를 검색해서 사용
 > 
 > __IS NULL = NaN (Not a Number) 결측값__
 
 
      SELECT *
      FROM Customers
      WHERE country LIKE 'Br%' 
      = 
      WHERE country = 'Brazil' ( 이 경우에는 정확한 DATA 명을 알고 있어야 함. / DATA 불러오는 속도가 훨씬 빠르다. )
      
      WHERE country LIKE 'B_____' ( ' _ ' = 빈칸을 의미 )
      
      SELECT *
      FROM Customers
      WHERE country IN ('Germany', 'France') =  WHERE country = 'Germany' OR country = 'France'
      
      SELECT *
      FROM Customers
      WHERE CustomerID BETWEEN 3 AND 5

___

#### BETWEEN  


> BETWEEN은 특정 범위 내에 있는 행만 추출  
> AND연산자와 함께 시작값, 끝값을 포함

    SELECT * 
    FROM CUSTOMERS
    WHERE CustomerNAME BETWEEN 'C' AND 'E';
  

#### IN

> IN은 값 목록을 지정  

    SELECT *
    FROM Customers
    WHERE Country IN ('Germany', 'France', 'Korea')
    
    
## DISTINCT
> 중복된 값을 제외시켜준다

    SELECT DISTINCT *
    FROM CUSTOMERS
    WHERE COUNTRY LIKE '%a%'
    OR COUNTRY LIKE '%b%'
    
    
## 데이터 순서 정렬하기
> 오름차순 정렬 : __ASC__  = Default값 
> 내림차순 정렬 : __DESC__  
> __ORDER BY__

    SELECT *
    FROM Customers
    * WHERE ___  조건절의 위치
    ORDER BY CustomerID DESC
    
    
    SELECT * 
    FROM Products
    WHERE price >= 88
    ORDER BY Price DESC
    
    
    
## 문자열 자르기  
> LEFT / RIGHT : ( 컬럼명 또는 문자열, 문자열의 길이 )  
> SUBSTRING : ( 컬럼명 또는 문자열, 시작 위치, 길이 ) =; SUBSTR

  
     SELECT LEFT ( "20140323", 4 ) => 2014
     
     SELECT RIGHT ( "20140323", 4 ) => 0323
     
     SUBSTR ( "20140323", 1, 4 ) => 2014
     SUBSTR ( "20140323", 5 ) => 0323






