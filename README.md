# fastai-docker
Docker images for fastai v3 course

cpu - directory with Dockerfiles for cpu only images
amd - directory with Dockerfiles for amd ROCm images


To use these images, download and install docker from docker.com.  Start the docker service and then at the command line 
run `docker pull ssthapa/fastaiv3:cpu-0.0.1` .  Once that is done, run `docker images` and get the image id associated 
with the ssthapa/fastaiv3 repository.  Then run `docker run -p 8888:8888 [ImageId]` replacing \[ImageId\] with the image 
id you got from the `docker images` command.  The `docker run` command should have printed an url starting with 
http://127.0.0.1:8888 , copy the *entire* url and visit it in a browser.
