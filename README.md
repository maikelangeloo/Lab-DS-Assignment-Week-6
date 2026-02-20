# Lab-DS-Assignment-Week-6

## Dataset
Name: Cuisine_rating
Source: Kaggle

## Steps Performed
- Loaded dataset
- Examined structure and summary statistics
- Checked missing values
- Visualized distributions and relationships

## R Code
library(tidyverse)

data <- read.csv("LAB DATA EDA - Copy/DATASET/Cuisine_rating.csv")

names(data)

str(data)

summary(data)

colSums(is.na(data))

ggplot(data, aes(x = Budget)) + geom_histogram(bins = 10)

ggplot(data, aes(y = `Food.Rating`)) + geom_boxplot()

cor(data[, c("Budget", "Food.Rating", "Service.Rating", "Overall.Rating")])
