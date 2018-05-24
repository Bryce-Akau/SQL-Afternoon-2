SYNTAX HINT
SELECT [Column names] 
FROM [Table] [abbv]
JOIN [Table2] [abbv2] ON abbv.prop = abbv2.prop WHERE [Conditions];

SELECT a.Name, b.Name FROM SomeTable a JOIN AnotherTable b ON a.someid = b.someid;
SELECT a.Name, b.Name FROM SomeTable a JOIN AnotherTable b ON a.someid = b.someid WHERE b.email = 'e@mail.com';

QUESTION 1
SELECT *
FROM Invoice AS i
JOIN InvoiceLine AS il
ON il.invoiceId = i.invoiceId
WHERE il.UnitPrice > 0.99;

QUESTION 2
SELECT i.InvoiceDate, c.FirstName, c.LastName, i.Total
FROM Invoice i
JOIN Customer c
ON i.CustomerId = c.CustomerId

QUESTION 3
SELECT c.FirstName, c.LastName, e.FirstName, e.LastName
FROM Customer c
JOIN Employee e
ON c.SupportRepId = e.EmployeeId

QUESTION 4
SELECT al.Title, ar.Name
FROM Album AS al
JOIN Artist AS ar
ON al.ArtistId = ar.ArtistId

QUESTION 5
SELECT pt.TrackId
FROM PlaylistTrack AS pt
JOIN Playlist AS p
ON pt.PlaylistId = p.PlaylistId
WHERE p.name = 'Music'

QUESTION 6
SELECT t.name
FROM Track AS t
JOIN PlaylistTrack AS p
ON t.TrackId = p.TrackId
WHERE p.PlaylistId = 5

QUESTION 7
SELECT t.name, p.name
FROM Track AS t
JOIN PlaylistTrack AS pt
ON t.TrackId = pt.TrackId
JOIN Playlist AS p
ON pt.PlaylistId = p.PlaylistId

QUESTION 8
SELECT t.name, al.title
FROM Track AS t
JOIN Album AS al
ON t.AlbumId = al.AlbumId
JOIN Genre AS g
ON t.GenreId = g.GenreId
WHERE g.name = 'Alternative'