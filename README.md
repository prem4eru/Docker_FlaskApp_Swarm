# Simple Docker Flask App using Swarm and Docker Compose 
There are below steps to run the applications 
1. sudo docker build -t flaskimage .
2. docker swarm init
3. docker network create --driver overlay flasknetwork (Any name) 
4. docker network ls
5. docker service create --replicas 3 --network flasknetwork -p 5000:5000 --name flaskservice flaskimage

Open a browser and run http://localhost:5000 to see the output 
If you are running the application on Ec2 instance run https://PublicIP_of_Ec2:5000 to check the output

*************************Output**************************
                     Hello World 
