Steps :

1. build the container image and give it the name hello-virtualization
    docker build . -t hello-SimpleTimeService
   
2. Build our container image. To run the image we simply type:
   docker run hello-SimpleTimeService

3. tag the container image:
   docker tag hello-virtualization:latest https://hub.docker.com/u/sneha199509/hello-SimpleTimeService:latest

4. push the image to Docker Hub:
   docker push https://hub.docker.com/u/sneha199509/hello-SimpleTimeService:latest

5. Create a manifest file called SimpleTimeService.yaml to create a Deployment for our app:

6. to run the manifest file
   kubectl apply -f SimpleTimeService.yaml

7. create manifest file for Kubernetes Services:
   kubectl apply -f Service.yaml

8. to run the container and see the output use below :
   kubectl run SimpleTimeService --rm -i --tty --image curlimages/curl -- sh
