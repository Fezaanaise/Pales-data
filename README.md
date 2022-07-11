# Pales-data
This is the second time I am attempting to configure Git knowledge.
Third edits
library(dplyr)

library(readr)

library(ggplot2)
library(ggthemes)
getwd()
setwd("~/Users/user/Documents")
getwd()
setwd("~/Downloads")
getwd()
Palestinians<-read.csv('Palestinian_victims.csv',header=TRUE, sep = ",")


summ_year<-Palestinians%>%
  select(Year,Palestinians.Killed,Israelis.Killed)%>%
  group_by(Year)%>%
  summarise(summp=sum(as.integer(Palestinians.Killed), na.rm = TRUE),
            summi=sum(as.integer(Israelis.Killed),na.rm=TRUE))

# Number of Palestinians killed
df1 <- Palestinians%>%  
  select(Year, Palestinians.Killed)
  
  


%>% # Use only variables year and number killed
  group_by(Year) 


# Same process but now with Israelis killed
df2 <- Palestinians%>%  
  select(Year, Israelis.Killed)
df3<-data.frame(df1)

%>% # Use only variables year and number killed
  group_by(Year)
  
  
# I don't know what is going on here but I guess we will find out. 





# Join df1 and df2 by Year

df5<-data.frame(df1,df2)

df4%>%
  group_by(Year)%>%
  tally()

trial<- Palestinians%>%
   select(Year,Palestinians.Killed, Israelis.Killed)%>%
   group_by(Year, Palestinians.Killed, Israelis.Killed)%>%
   summarise(summation= sum(Year))
  
ggplot()+ geom_line (data=summ_year, mapping = 
       aes(x=Year,
           y=summp, color="red") + geom_line(data=summ_year,mapping = 
                                aes(x=Year,
                                    y=summi, color="blue"))+labs(x="Year", y="summp (red), summi(blue)" )
                                  
                                  
                                  
            





           
