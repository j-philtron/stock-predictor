# HW Week 12 addendum
Below are the answers to the associated questions for week 12's homework assignment.

## The questions and the answers:

1. What does it mean to create a Docker image and why do we use Docker images?

 - A docker image is a snapshot of the app ready to run. It is a file that is ready to be used to execute code within a Docker container. We use them because they are fully set-up instructions for how the code should run. The image contains the application and all of the dependencies required to run it.

2. Please explain what is the difference from a Container vs a Virtual Machine?

 - They are similar in that both are methods that allow apps to be run in a closed environment. However, virtual machines (VMs) include an operating system, while Docker containers share the host OS kernel. VMs are slower, since they need to start the entire OS. Docker containers are more portable, since the container image can be run in any host environment and it is smaller than a VM since it doesn't have a copy of the OS.


3. What are 5 examples of container orchestration tools (please list tools)?

 - Five container orchestration tools are: Kubernetes, Openshift, Mesos, Mirantis, and Google Container Engine (GKE). There are many more tools out there!


4. How does a Docker image differ from a Docker container?

 - A Docker image is a file that describes the app and how it can be run, while a Docker container is the runtime instance of the image. 

