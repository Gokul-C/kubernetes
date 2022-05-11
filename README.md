# First deploy secret file  
secret file contains all the credentials of mongodb .

# Secondly deploy the mongo-deployment file

it contains all the configuration of image and pod and also contains service file in same file . 

service file contains the information to talk with pods . 

# Now deploy mongo-configmap file 
Its an mongo-express file , in this file we represent to which database this mongo-express should connect . 

# Finally deploy mongo-express.yaml 

It contains all the mongo express configuration and this file aslo contains service file , In this we represent 
all the ports need to be connect with external internet . 

# Then , after all files are launched using kubectl 

 Now , Still ip address is not  assigned to the minikube so we use the following command to start the service 
 of mongo-express . 
 
       $ minikube service mongo-express-service 
 
 This command will assign an ip address to the pod .
 
 So that we need to check ip addr of the minikube , for that : 
 
     $ minikube ip
     
 Now open any browser then type : 
 
     ipadress:port
     For ex : 192.168.0.1:30000
     
 Now you can see that mongodb is created and mongo-express is connected to mongodb and can communicate each other 
 perfectly . 
