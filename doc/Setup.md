#   Setup
Debian is suggested as base image by Docker documentation.

##  Jenkins
See official Jenkins image: https://github.com/jenkinsci/docker
Used Debian as base image and installed Jenkins manually.
Consider to use the official Jenkins Dockerfile and modify to use Debian and install Java.

##  Jenkins Volume
A data only container is used for the Jenkins image.
As suggested by several sources,
the Jenkins image is used as base image for the Valume container.
Reasons:
- It will not take more disk space, because of the Docker image layer characteristics 
- The image gets a chance to seed the volume with data such as default files
- The permissions and owners will be correct

See: http://container42.com/2014/11/18/data-only-container-madness/ and
http://stackoverflow.com/questions/25845785/most-appropriate-container-for-a-data-only-container
