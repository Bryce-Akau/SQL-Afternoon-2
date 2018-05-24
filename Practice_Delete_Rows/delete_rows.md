SYNTAX HINT
DELETE FROM [Table] WHERE [Condition]

DROP TABLE IF EXISTS practice_delete;

CREATE TABLE IF NOT EXISTS practice_delete ( Name string, Type string, Value integer );
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "bronze", 50);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "bronze", 50);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "bronze", 50);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "silver", 100);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "silver", 100);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "gold", 150);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "gold", 150);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "gold", 150);
INSERT INTO practice_delete ( Name, Type, Value ) VALUES ("delete", "gold", 150);

SELECT * FROM practice_delete;
/* Use this to filter out to find 1 set thing */
/* WHERE Type = 'silver'; */

QUESTION 1
DELETE 
FROM practice_delete
WHERE Type = 'bronze';

QUESTION 2
DELETE
FROM practice_delete
WHERE Type = 'silver';

QUESTION 3
DELETE
FROM practice_delete
WHERE Value = 150;

/* Will show the table after the delete */
SELECT * FROM practice_delete;