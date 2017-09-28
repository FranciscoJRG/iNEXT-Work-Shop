# iNEXT-Work-Shop
Using the iNEXT (Chao y Hsieh 2014) package for R
Hi there!

I'm trying to import my own data into the iNEXT library but it has been really difficult to me.
The script is as follows according to the tutorial


getwd() #This one, to know what was my root directory
setwd(dir = "C:/...direction.../Final folder") #I just set my root directory to work from here from now on
library(iNEXT) #Call the directory
library(ggplot2)
data(spider) # The tutorial says that use this comand to call the data. But here is where stats the troubles for me, actually I have my data in my root directory and I haven't been able to call and use the data

abundancias<-read.table(file = "zonas.txt") # now I called my date
save(abundancias, file = "zonas.rda") # I just saved into a .rda file
str(zonas)

iNEXT(zonas, q=0, datatype = "abundance") #ACTUALLY IT'S NOT WORKING FROM HERE ON.

m<-c(1,5,20,50,100,200,400)
iNEXT(zonas, q=0, datatype = "abundance", size=m)
out<- iNEXT(iNEXT zonas, q=c(0,1,2), datatype = "abundance", size = m)
ggiNEXT(out, type = 1, facet.var = "site")
ggiNEXT(out, type = 1, facet.var = "order")
ggiNEXT(out, type = 2)
ggiNEXT(out, type = 3, facet.var = "site")
ggiNEXT(out, type = 3, facet.var = "order")

