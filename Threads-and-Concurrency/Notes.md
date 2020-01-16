# Threads and Concurrency:
#### Scale out via the Process Model
* The Process Model states that an app should be able to scale out both **processes** and **process types**.
  * Based on the Unix Process Model for running service daemons:
    * service daemons should be a managed process. It should run automatically when the OS starts, and should be restarted if the process crashes or dies.
    * A service daemon like memcached has a single entry point, meaning it is invoked by a single command.
      * Contrastingly, web apps generally have >1 entry points. Each entry point is known as a **process type**.
    * Process Types should be declared like we declare our app dependencies.
      * Devs should be able to view process architecture.
* Process Types vs. Processes:
  * Process Types:
    * The prototype from which more processes are intitiated. Similar to the relationship between classes and objects in object-oriented programming.
    * scale when a new work specialization is needed.
  * Processes:
    * scale when more concurrency is needed.
* Basically, we assign each type of work to its own process type.
  * A VM can only grow so large. So we must be able to support many processes (containers) and types (images).

#### Action Items:
* Microservice architecture lends itself to this idea perfectly.
  * The processes are the equivalent to containers in Docker.
    * Each container runs a single image. There should be multiple containers for each image, spread across multiple AZ's, that are scalable.
  * Each image used in an application has its own responsibility. Separate from the responsibilities of other images.
    * New image types equate to new process types.
    * Ex: When a persistent data store is needed, we add a cockroach image with associated set of containers to the application.
      * This containers responsibilites are completely separate from the frontend containers, the redis containers, etc...

