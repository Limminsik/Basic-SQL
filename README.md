# Basic-SQL

## 0914
  HackerRank https://www.hackerrank.com/domains/sql
  
  W3school https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all
  
  ---

_* = 모든 것을 의미 ( 아스타 )_

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
