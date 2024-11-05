# Zuber-Ride-Sharing
Analysis of Zuber Ride Sharing Company in Chicago.
Data sourced from Zuber dataset which includes trips, cabs, weather records, and neighbor hoods.
Exploratory data analysis question: For each hour, retrieve the weather condition records from the weather_records table. Using CASE operator, break all hours into groups: "Bad" if the description field contains the words "rain" or "storm", and "good" for others example:
SELECT 
    ts,
    CASE 
        WHEN description LIKE '%rain%' OR description LIKE '%storm%' THEN 'Bad'
        ELSE 'Good'
    END AS weather_conditions 
FROM 
    weather_records;
  Exploratory data analysis question:  Retrieve the identifiers of O'Hare and Loop neighborhoods from the neighborhoods table example:
  SELECT
    neighborhood_id, 
    name
FROM 
    neighborhoods
WHERE 
    name LIKE '%Hare' OR name LIKE 'Loop'
    
