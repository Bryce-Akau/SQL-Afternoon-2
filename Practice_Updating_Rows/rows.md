SYNTAX HINT
UPDATE [Table] 
SET [column1] = [value1], [column2] = [value2] 
WHERE [Condition];

UPDATE Athletes SET sport = 'Picklball' WHERE sport = 'pockleball';

QUESTION 1
UPDATE Customer
SET Fax = null
WHERE Fax IS NOT null

QUESTION 2
UPDATE Customer
SET Company = 'Self' 
WHERE Company IS null

QUESTION 3
UPDATE Customer
SET LastName = 'Thompson'
WHERE FirstName = 'Julia' AND  LastName = 'Barnett'

QUESTION 4
UPDATE Customer
SET SupportRepId = 4
WHERE Email = 'luisrojas@yahoo.cl'

QUESTION 5
UPDATE Track
SET Composer = 'The darkness around us'
WHERE GenreId = ( SELECT GenreId FROM Genre WHERE Name = 'Metal' )
AND Composer IS null;