Code for exercise of course R Programming / Código para el ejercicio de R Programming

CÓDIGO PARA CREAR LA FUNCIÓN POLLUNTANTMEAN DEL CURSO R PROGRAMMING

A continuación se comparte el código creado para la función POLLUNTANTMEAN, ( se comparte diagrama de flujo).  Si alguien encuentra alguna mejora es totalmente bienvenida.

In the next lines you can see the code written for create the function POLLUNTANTMEAN (also I share the diagram). If someone finds one improve, it's totally welcome


########### POLLUTANMEAN #################
##########################################
##### AUTHOR: ESAÚ CONTRERAS
##### DATE : 2019-08-24
##### DESCRIPTION: FUNCTION FOR READ FILES AND CALCULATE
##### THE AVERAGE OF THE DETERMINED COLUMN
##########################################

 #GET DIRECTORY
getwd()

 #SAVE THE PATH IN AN OBJECT
path<-"C:/Users/PC/Documents/specdata/"
path

 #SAVE THE FILES IN DIRECTORY IN AN OBJECT
files<-list.files("C:/Users/PC/Documents/specdata/")
files
	
 #FUNCTION DEFINITION
pollutantmean<-function( path, pollutant, id=1:332) {
data2<-data.frame()
path<-"C:/Users/PC/Documents/specdata/"
	for (i in id){
		data<-read.csv(paste0(path,files[i]),header=TRUE)
	data2<-rbind(data2,data)
}
mean(data2[,pollutant], na.rm=T)
}

 #TEST FUNCTION
pollutantmean(path,"nitrate",70:72)
