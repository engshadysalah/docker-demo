## By Shady Salah



## Description

   -  It’s required to do the following from ​ Console ​ :
   
       ## [1]: Create a Docker image that has ​Nginx installed from base ​centos ​image on your local machine.

 

## Prerequisites

  - 01: Install Docker.
  


## [ECT-015] Resources:

  ## [1]: Create a Docker image that has ​Nginx installed from base ​centos ​image on your local machine.

   - 01: Create a base centos ​image, [docker-demo/centos-7-image/Dockerfile]

         - Build the Image:
                             - $ cd docker-images/centos-7-image
                             - $ docker build -t new-demo-centos-7 .

                             - .  means build the image inot current path.
                             - add [centos-7-x86_64-docker.tar.xz] into same dir because the image needs it.


         - Remove Image by id:
                              - $ docker rmi  <image-id>
                              - $ docker rmi -f <image-id>


         - Remove Conatiner by id:
                              - $ docker rm  <conatiner-id>
                              - $ docker rm -f <conatiner-id>
  


   - 02: Create a Docker image that has Nginx installed from base ​[centos:centos7] centos image, [docker-images/nginx-image/Dockerfile]

            - Build the Image:
                                - $ cd docker-images/nginx-image
                                - $ docker build -t new-demo-nginx .
            
            - Run the image just execute:

                                - $ docker run -d -p 80:80 new-demo-nginx



    - 03: Then can access the URL of nginx based on the [nginx.conf]
      
                              - index.html: http://localhost/

                              - error page:  http://localhost/XxX



  ## [2]: Push your image to Docker Hub.


   - 01: Log in into your registery:

                              - $ docker login


   - 02:Add tag to your image with your repo:

                              - $ docker tag new-demo-nginx shadysalah297/common-repo:new-demo-nginx



   - 03: Push it into your registery:


                               - $ docker push shadysalah297/common-repo:new-demo-nginx



## Get Started and check the Acceptance Criteria

   To get started, Please Follow the next steps...
 
   - 01: Test Docker image that has ​Nginx installed from base ​centos ​image on your local machine. 
   
              - Access the URL of nginx based on the [nginx.conf]
      
                    - index.html: http://localhost/

                    - error page:  http://localhost/XxX


  
## Important Note:

     [01]: Create a Docker image that has ​Nginx installed from base ​centos ​image on your local machine.
           - That means the Docker image that has ​Nginx can be build with docer and it contains the centos ​image on your local machine, So we don't need centos ​image.
           - So When I build the Docker image that has ​Nginx on the AWS ECS, It working will without build the centos ​image.
 


## References:

    [1]: Docker Installation, https://docs.google.com/presentation/d/1iPEuT3owDif4_IzysuQbAwJMyq389T87nu2X6yHXtBg/edit#slide=id.g8707078a9b_0_403

    [2]: Base Image, https://docs.docker.com/develop/develop-images/baseimages/

    [3]: Create base ​ centos ​ image, https://hub.docker.com/_/centos [and] https://buildlogs.centos.org/centos/7/docker/
