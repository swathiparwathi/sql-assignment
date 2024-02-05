# sql-assignment

1)
SELECT
  unique_key FROM `bigquery-public-data.austin_incidents.incidents_2008`
WHERE descript = 'DWI' LIMIT 10;

https://drive.google.com/file/d/1f2dzPZ07lPzfqy5tHg-FHcTWtACbcUm-/view?usp=sharing

2)
SELECT address
FROM `bigquery-public-data.austin_incidents.incidents_2008` LIMIT 10;

https://drive.google.com/file/d/1Om_I8y8LNd279ELj4t9FC0yCPVwVPKL1/view?usp=sharing


3)
SELECT
  DISTINCT descript FROM `bigquery-public-data.austin_incidents.incidents_2008` LIMIT 10;

https://drive.google.com/file/d/1Qzi_D9-HCj0Z3EMtzxZHG5W-QBuHp_w8/view?usp=sharing

4)
SELECT
  COUNT(*)
FROM
  `bigquery-public-data.austin_incidents.incidents_2008` 
WHERE
  longitude IS NOT NULL
  AND latitude IS NOT NULL
  AND location IS NOT NULL 
  LIMIT 10;

https://drive.google.com/file/d/1v8izqUgckSgjsZXgBPW3Rs6wLPAKH2BE/view?usp=sharing


5)
SELECT date,time
FROM
  `bigquery-public-data.austin_incidents.incidents_2008`
WHERE
  address LIKE '5100%' LIMIT 10;


https://drive.google.com/file/d/1sOCF7Avgvpgw1H3MRGc3LCDSdhxhxtDA/view?usp=sharing


6)
SELECT
  MAX(time) FROM
  `bigquery-public-data.austin_incidents.incidents_2008` LIMIT 10;

https://drive.google.com/file/d/1zrYczdwD-xB0GG2u31zzrcOohLKn6L3D/view?usp=sharing





7)
SELECT * FROM `bigquery-public-data.austin_incidents.incidents_2008`
WHERE
  descript = 'THEFT'
  AND unique_key > 20082021744 
  LIMIT 10;

https://drive.google.com/file/d/1ZLmcJ1A6sYWd6eqotQjTXjiM10uVsFHX/view?usp=sharing


8)
SELECT address
FROM `bigquery-public-data.austin_incidents.incidents_2008`
ORDER BY
  time DESC
LIMIT 10;
  #Joint Query

https://drive.google.com/file/d/1vAIrulAihcLLDQ7efykmE6twxnQpLQXl/view?usp=sharing



9)
SELECT * FROM `bigquery-public-data.austin_incidents.incidents_2008` 
t1
LEFT JOIN
  `bigquery-public-data.austin_incidents.incidents_2010` t2
ON
  t1.time = t2.time
WHERE
  t1.time > '11:00:00'
LIMIT
  10;

https://drive.google.com/file/d/1ZBAnx7txFf28x7eClSmMXE-vxJ5pBt2u/view?usp=sharing

10)
SELECT
  t1.descript
FROM
  `bigquery-public-data.austin_incidents.incidents_2008` t1,
  `bigquery-public-data.austin_incidents.incidents_2009` t2
WHERE
  t1.latitude = t2.latitude
  AND t1.longitude = t2.longitude
LIMIT
  10;


https://drive.google.com/file/d/18hXMHgyS9hTNeObT-88TOqqI6mVw3OUU/view?usp=sharing

