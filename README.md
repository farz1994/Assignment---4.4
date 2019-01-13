Use the package RcmdrPlugin.IPSUR. data(RcmdrTestDrive) and perform the below operations:
library(RcmdrPlugin.IPSUR)
View(RcmdrTestDrive)
data("RcmdrTestDrive")

a. Calculate the average salary by gender and smoking status.
a <- tapply(RcmdrTestDrive$salary, list(RcmdrTestDrive$gender, RcmdrTestDrive$smoking), mean, na.rm =T)
> a
       Nonsmoker   Smoker
Female  692.9093 733.2122
Male    740.9080 751.4900

b. Which gender has the highest mean salary?
b <- tapply(RcmdrTestDrive$salary, RcmdrTestDrive$gender, mean, na.rm =T)
> b
  Female     Male 
698.0911 743.3915
> Male has the highest mean salary

c. Report the highest mean salary.
> 743.3915

d. Compare the spreads for the genders by calculating the standard deviation of salary by gender.
d <- tapply(RcmdrTestDrive$salary, RcmdrTestDrive$gender, sd, na.rm =T)
> d
  Female     Male 
130.7053 158.5423 
