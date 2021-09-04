
library(openxlsx)
D <- read.xlsx("data.xlsx")
head(D)
X<-unlist(D[1,2:30])
Y<-unlist(D[2,2:30])
plot(X,Y,main="好きなグラフのタイトル", col="red")

fm<-nls(Y~c /(1+ exp( -X * a - b ))+d,start=c(a=1,b=1,c=1,d=1),trace=TRUE)
lines(X,fitted(fm), col="blue", lwd=5)


#plot(X,log10(Y))
#lines(X, log10(fitted(fm)))