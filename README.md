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







**DECLARE @BatchSize INT = 1000;
DECLARE @Offset INT = 0;
DECLARE @TotalIterations INT;

SELECT @TotalIterations = CEIL(COUNT(*) / @BatchSize)
FROM your_table;

DECLARE @CurrentIteration INT = 1;

WHILE @CurrentIteration <= @TotalIterations
BEGIN
  -- Process current batch
  SELECT *
  FROM your_table
  ORDER BY your_column
  LIMIT @BatchSize
  OFFSET @Offset;

  -- Increment offset and iteration
  SET @Offset = @Offset + @BatchSize;
  SET @CurrentIteration = @CurrentIteration + 1;
END**

    
