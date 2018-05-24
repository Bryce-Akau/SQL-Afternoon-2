SYNTAX HINT
SELECT [Column names] 
FROM [Table] 
WHERE ColumnId IN ( SELECT ColumnId FROM [Table2] WHERE [Condition] );

SELECT Name, Email FROM Athlete WHERE AthleteId IN ( SELECT PersonId FROM PieEaters WHERE Flavor='Apple' );

QUESTION 1
SELECT *
FROM Invoice
WHERE InvoiceId
IN (
  SELECT InvoiceId
  FROM InvoiceLine
  WHERE UnitPrice > 0.99
);

QUESTION 2
SELECT *
FROM PlaylistTrack
WHERE PlaylistId
IN (
  SELECT PlaylistId
  FROM Playlist
  WHERE Name = 'Music'
);

QUESTION 3
SELECT Name
FROM Track
WHERE TrackId
IN (
  SELECT TrackId
  FROM PlaylistTrack
  WHERE PlaylistId = 5
);

QUESTION 4
SELECT *
FROM Track
WHERE GenreId
IN (
  SELECT GenreId
  FROM Genre
  WHERE Name = 'Comedy'
);

QUESTION 5
SELECT *
FROM Track
WHERE AlbumId
IN (
  SELECT AlbumId
  FROM Album
  WHERE Title = 'Fireball'
);

QUESTION 6
SELECT *
FROM Track
WHERE AlbumId 
IN (
  SELECT AlbumId
  FROM Album
  WHERE ArtistId
  IN (
    SELECT ArtistId
    FROM Artist
    WHERE Name = 'Queen'
  )
);