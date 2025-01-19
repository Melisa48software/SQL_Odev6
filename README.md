# SQL_Odev6
lcw bootcamp sql 6.ödev reposudur.

-- 1. Film Tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?
SELECT AVG(rental_rate) AS average_rental_rate
FROM film;

-- 2. Film Tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?
SELECT COUNT(*) AS count
FROM film
WHERE title LIKE 'C%';

-- 3. Film Tablosunda bulunan filmlerden rental_rate değeri 0.99'a eşit olan en uzun (length) film kaç dakikadır?
SELECT MAX(length) AS longest_movie_length
FROM film
WHERE rental_rate = 0.99;

-- 4. Film Tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?
SELECT COUNT(DISTINCT replacement_cost) AS distinct_replacement_cost_count
FROM film
WHERE length > 150;

