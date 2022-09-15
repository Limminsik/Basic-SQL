# Basic-SQL
  HackerRank   https://www.hackerrank.com/domains/sql
  
  W3school     https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all
  
  ---

> __* = 모든 것을 의미 ( 아스타 )__

      SELECT *  
      FROM Customers
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


## WHERE 절 요약
    
    
