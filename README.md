# Haiku
## Weather Data haiku

#### Created by Sonja Janssen-Sahebzad

## Load necessary packages
library(stringr)
library(magrittr)

## Simulated weather data
weather_data <- data.frame(
    date = seq(as.Date("2023-01-01"), as.Date("2023-01-07"), by = "days"),
    temperature = c(10, 12, 11, 9, 8, 7, 6),
    precipitation = c(0, 0, 2, 1, 0, 0, 3)
)

## Extract relevant weather information
avg_temp <- mean(weather_data$temperature)
total_precipitation <- sum(weather_data$precipitation)

## Create a haiku
haiku <- str_wrap(
    paste(
        "Amidst winter's chill,", 
        "Subdued warmth, soft rains embrace,", 
        "Nature's quiet grace."
    ),
    width = 30
)

## Display the haiku with weather data
cat("Average Temperature:", avg_temp, "°C\n")     
cat("Total Precipitation:", total_precipitation, "mm\n\n")  
cat(haiku)


 
## Outcome:

### "Amidst winter's chill, Subdued
###   warmth, soft rains embrace,
###   Nature's quiet grace."
###   Average Temperature: 9 °C
###   Total Precipitation: 6 mm


