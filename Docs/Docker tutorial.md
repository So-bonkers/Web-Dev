# Docker Tutorial

## Course Overview

1. What is Docker? What is a Container?
2. Docker vs Virtual Machine
3. Docker Installation
4. Main Commands
5. Debugging a Container
6. Developing with Containers
7. Docker Compose - Running multiple services
8. Dockerfile - Building own Docker image
9. Private Docker repository - AWS
10. Deploy the Containerized App
11. Volumes - Persisting Data
12. Volumes Demo
    
### What is Docker? What is a Container?

**What is a Container?**

* A way to **package** application with **all** the **necessary dependencies** and **configuration**
* **Portable artifact**, easily shared and moved around b/w development team or development and operations team
* This portability of containers with everything packaged in one isolated environment gives it some advantages that make development and deployment **more efficient**

### Where do containers live?

Containers are portable, so there must be some kind of a storage for those containers, so that you can share them and move them around. So containers live in a :
* Container Repository
* Private repositories
* Public repository for Docker

### How containers improved the application development experience

1. **Before Containers**:
   * Developers would have to install most of the dependencies on their operating systems directly.
   * They'd have to install the binaries of those services and configure them and run them on their local development environment
   * Depending on which OS is used **the installation process differs**
   * **Many steps** where something could go wrong

2. **After containers**:
   * You actually do not have to install any of the services directly on your OS because the container because the container is its own isolted environment
   * It is shipped/packaged with all needed configuration
   * The download step is just one Docker command to install the app which fetches the container and starts it at the same time; the command is same regardless of which OS you are using
   * You can have 2 different versions of the same applications running on your local environment without having any conflict

### How containers improved the application deployment experience

1. **Before containers**:
   * Dev team will produce artifacts together with a set of instructions of how to install and configure those artifacts on the server
   * So, you would typically have a jar file for your application and in addition, you would have some kind of a database service also with a set of instructions of how to configure and set it up on the server
   * So, Dev team will give those artifacts to Ops team, which will handle setting up the environment to deploy.
   * Here, some of the noticable disadvantages are:
     * You need to configure and install everything