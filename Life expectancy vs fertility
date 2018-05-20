library(dplyr)
library(ggplot2)
library(dslabs)
data(gapminder)
## fill out the missing parts in filter and aes
gapminder %>% filter(year == 2012 & continent == "Africa") %>%
  ggplot(aes( fertility ,life_expectancy )) +
  geom_point()
  
gapminder %>% filter(year == 2012 & continent == "Africa") %>%
  ggplot(aes(fertility, life_expectancy, color = region)) +
  geom_point()
  
#Create a table showing the country and region for the 
#African countries (use select) that in 2012 had fertility rates of 3 or less and life expectancies of at least 70.  
df <- gapminder %>% filter(continent=="Africa"&year==2012&fertility<=3&life_expectancy>=70) %>%     select(country, region)

#Use filter to create a table with data for the years from 1960 to 2010 in Vietnam and the United States.
list_country <- c("Vietnam","United States")
tab <- gapminder %>% filter(country%in%list_country,year>=1960 & year <=2010)
