<div align="center">
  <a href="https://github.com/Krishnamohan-Yerrabilli/Kubernetes-hands-on">
    <img src="https://user-images.githubusercontent.com/58173938/196433324-45e814cb-fb4d-4807-9134-af30e45e9ea6.png" alt="kuber" width="200" height="200">
  </a>
</div>
<br>
<div align="center">
This repo consists of all my learnings, I explained different concepts in detail with practical <br>
exposure, feel free to fork, if you like my work leave a ⭐ <br>Thank you, happy learning :)
</div>
<br>

# Kubernetes-hands-on

## What is Kubernetes?

Kubernetes is an open-source platform "Orchestration engine" mainly used to manage
containerized applications, it is released by Google in 2014, and the project is donated 
to CNCF (Cloud-native computing foundation), primarily it serves micro-services applications,
and it is still the world's second-biggest project in open source after Linux.


## Why use Kubernetes?

An orchestration engine helps to watch and control containerized applications very closely, 
and it is also used to automate certain functions, let me give an example for a better 
understanding this broad topic, Let's say one of your application service's containers went down,
it's not such a big deal to manually restart the container, but what if a large number of containers
went down suddenly, wouldn't be easy this task will be automatically done, this is where Kubernetes comes, k8's will restart the containers, not only that it also provides many services such as logging,
load balancing, secret, scheduling, scaling, fault-tolerance, deployment.

## Kubernetes architecture

<div align="center">
  <a href="https://github.com/Krishnamohan-Yerrabilli/Kubernetes-hands-on">
    <img src="https://storage.googleapis.com/algodailyrandomassets/curriculum/software-engineering/kubernetes/Architecture.png" alt="kuber" width="800" height="500">
  </a>
</div>
<br>

### Brief 

Kubernetes architecture has the master node, which is also called as control plane nowadays, 
which controls the nodes.these nodes are nothing but physical servers or VMs, which are run 
inside a data center applications are run inside the node, these nodes are previously called 
minions, In that, we have a lot of components such as type of service, cluster, pod. 

### Master Node aka (Control plane)

<br>
<div align="center">
  <a href="https://github.com/Krishnamohan-Yerrabilli/Kubernetes-hands-on">
    <img src="https://startkubernetes.com/static/7b7a66152f804ca26d48493975f99124/29be2/k8s-master.png" alt="kuber" width="800" height="500">
  </a>
</div>
<br>

The Control plane acts like a mother to all worker nodes, It is responsible for doing many 
operations, such as scheduling worker nodes, taking control of the whole cluster, majorly 
it has 4 components API server, control manager, etcd, scheduler, the primary component 
in the cluster is the API server which communicates with the host and many other parts in 
the cluster, the control manager takes control of the fault tolerance, and many more, such 
as if any pods(which we see in a bit), etcd holds our desired state data(YAML files which we
 see in a bit), and scheduler which schedules pods on available nodes.

### Components of the Master Node

#### API server

API server acts like the heart of the cluster, without API services we can't interact with k8's 
cluster, The role of the API server is to communicate with other components in the cluster, 
such as scheduler, etcd, control manager, kubelet, kube-proxy it's mandatory to communicate 
to have API server in between them.




