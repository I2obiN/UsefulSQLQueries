/****** Script for Deleting Duplicate Rows  ******/
WITH DUPLICATES AS
(SELECT Linkedin_URL, ROW_NUMBER() OVER (PARTITION BY Linkedin_URL ORDER BY (SELECT 0)) AS RN 
FROM CrawlerAcquisitionQueue WHERE Domain_Type = 'angellist.profile')
DELETE FROM DUPLICATES WHERE RN > 1
  
