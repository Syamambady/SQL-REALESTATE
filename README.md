# SQL-REALESTATE

# To view whole data
select * from realestate;

# Count of Properties in Each City

SELECT city, COUNT(*) AS property_count
FROM realestate
GROUP BY city;

#vAverage Price of Properties in Each City

SELECT city, AVG(price) AS avg_price
FROM realestate
GROUP BY city;

# Average Number of Bedrooms and Bathrooms in Each City

SELECT city, AVG(bed) AS avg_bedrooms, AVG(bath) AS avg_bathrooms
FROM realestate
GROUP BY city;

# Properties with Largest Acreage

SELECT *
FROM realestate
ORDER BY acre_lot DESC
LIMIT 10; -- Change the limit as needed

# Average House Size in Each City

SELECT city, AVG(house_size) AS avg_house_size
FROM realestate
GROUP BY city;

# Average Price per Acre in Each City

SELECT city, AVG(price / acre_lot) AS avg_price_per_acre
FROM realestate
GROUP BY city;

# Properties with Highest Price per Square Foot

SELECT *
FROM realestate
ORDER BY (price / house_size) DESC
LIMIT 10; -- Change the limit as needed

# Summary Statistics for Prices

SELECT 
    MIN(price) AS min_price,
    MAX(price) AS max_price,
    AVG(price) AS avg_price
FROM realestate;

# Properties with the Most Bedrooms:

SELECT *
FROM realestate
ORDER BY bed DESC
LIMIT 10; -- Change the limit as needed

# Properties with the Most Bathrooms:

SELECT *
FROM realestate
ORDER BY bath DESC
LIMIT 10; -- Change the limit as needed

# Average Price per Bedroom and Bathroom:

SELECT 
    AVG(price / bed) AS avg_price_per_bedroom,
    AVG(price / bath) AS avg_price_per_bathroom
FROM realestate;

# Properties with the Largest House Size:

SELECT *
FROM realestate
ORDER BY house_size DESC
LIMIT 10; -- Change the limit as needed

# Properties with the Lowest Price per Square Foot:

SELECT *
FROM realestate
ORDER BY (price / house_size) ASC
LIMIT 10; -- Change the limit as needed

