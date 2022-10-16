Before we work with K8s PV, some things to be noted
let's see what they are

Container: 

     - The container is just a running process
     - Container is ephemeral
     - when creating a container, Linux will assign a temporary file system, 
     - which is related to Linux namespaces, capabilities

State:

     - The state is normally just some form of data that our application needs to function
     - a container or pod or an application is just a running process, there are two types of process

Stateless:

     - A stateless process is a process that does depend on state or data to function 
     - It does not store any state or data in memory(main) or the filesystem(secondary)

Stateful:

     - The stateful process depends on the state to function, which will store in only two places
     - One is in memory and the other is on disk memory allows access to your data

So what makes containers different to other processes:

     - A container usually has its own file system when docker creates a container
     - it creates a virtual file system and attaches it to that container unlike processes 
     - on a host that have access to the whole file system 
     - containers have their own file system so when a container gets destroyed and recreated 
     - it loses the file system,  and the file system gets recreated against of files on lost 
     - therefore the container file system is not persisted during restarts

Let's see real world example, of how this thing works

Let's play with docker volumes:

I will update...
