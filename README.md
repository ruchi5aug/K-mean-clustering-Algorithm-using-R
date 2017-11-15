# K-mean-clustering-Algorithm-using-R 
table(iris)
row(iris)
head(iris)
New_iris<-iris
New_iris$Species=NULL
head(New_iris)
res<-kmeans(New_iris,3,iter.max = 10)
res
?kmeans
res
plot(iris[c("Sepal.Length","Sepal.Width")], col=res$cluster)
plot(iris[c("Petal.Length","Petal.Width")], col=res$cluster)
x<-table(iris$Species,res$cluster)
x
