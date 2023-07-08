# Technical-Documentation
Migration of  SQlite3Db to Postgresql in Django

UPDATE your_table t
JOIN (
    SELECT column1, column2, column3
    FROM your_table
    WHERE condition
) subquery
ON t.column1 = subquery.column1
    AND t.column2 = subquery.column2
    AND t.column3 = subquery.column3
SET t.column4 = subquery.column4,
    t.column5 = subquery.column5,
    t.column6 = subquery.column6;
