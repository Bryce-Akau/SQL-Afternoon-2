SYNTAX HINT
SELECT [Column1], [Column2]
FROM [Table] [abbr]
GROUP BY [Column];

QUESTION 1
SELECT COUNT(*), g.name
FROM Track AS t
JOIN Genre AS g
ON t.GenreId = g.GenreId
GROUP BY g.Name;

QUESTION 2
SELECT COUNT(*), g.Name
FROM Track AS t
JOIN Genre AS g
ON t.GenreId = g.GenreId
WHERE g.Name = 'Pop' OR g.Name = 'Rock'
GROUP BY g.name;

QUESTION 3
SELECT COUNT(*), a.Name
FROM Artist AS a
JOIN Album As al
ON a.ArtistId = al.ArtistId
GROUP BY al.ArtistId;