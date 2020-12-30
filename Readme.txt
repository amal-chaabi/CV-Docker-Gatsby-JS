###################################################################################################################################
                      Mini Projet DOCKER   Amal Chaabi 3 IDL 2
###################################################################################################################################




################## Développement ##################
   
   1- mkdir application                                                                                                                                  
   2- cd application                                                                                                                                     
   3- touch Dockerfile                                                                                                                             
   4- docker build -t myimg . 
   5- mkdir data 
   6- cd data 
   7- touch siteConfig.js                                                                   
   8- docker run -it -p 8000:8000 myimg                                                                                               
   9- docker run -it -p 8000:8000 -v ~/application/data:/user/src/application/mycontainer/data myimg           
   10- docker run -it -p 8000:8000 -v  ~/application/data:/user/src/application/mycontainer/data -v ~/application/images:/user/src/application/mycontainer/public/images myimg        





##################  Build ##################

   1- touch DockerfileBuild
   2- docker build -f DockerfileBuild -t myimg1 .                                                                                           
   3- docker run -it -v ~/application/data:/user/src/application/mycontainer/data -v ~/application/public:/user/src/application/mycontainer/public myimg1                  



################## Prod ##################
 
   1- touch DockerfileProd 
   2- docker build -f DockerfileProd -t myimg2 .                                      
   3- docker run -it -p 80:80  myimg2                                                

   

