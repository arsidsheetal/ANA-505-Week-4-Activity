# ANA-505-Week-4-Activity
ANA 505 Week 4 Activity with dplyr

#Week 4: dplyr package



mydata <- data.frame(HairEyeColor)



head(mydata,10)



install.packages("dplyr")
library(dplyr)



select(mydata, Hair, Sex)



newdata <- select(mydata, Hair = Hair, Sex = Sex)



newdata <- select(newdata, -Sex)



rename(mydata, Gender = Sex)



mydata[,"Gender"] <- NA
mydata



male_data <- filter(mydata, Sex == "Male")
male_data <- select(male_data, Sex)
male_data



group_by(mydata, Sex)

#After you run it, write the total here:592

total=mutate(mydata, total=cumsum(Freq))
total



female_data <- filter(mydata, Sex == "Female")
female_data <- select(female_data, Sex)
female_data



bind_rows(male_data,female_data)


#Here we are using 'arrange' function to arrange a dataframe with specific Column

arrange_mydata_by_hair<- arrange(mydata, Hair)
arrange_mydata_by_hair
