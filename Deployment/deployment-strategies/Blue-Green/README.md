![Untitled design (2)](https://user-images.githubusercontent.com/58173938/193967528-5f64dc54-4713-46b1-b472-fb1f275031e2.png)


## Introduction

A blue/green deployment involves deploying the new application version (green) beside with the old (blue).

A load balancer in the form of a Service Selector object is used to test and redirect traffic to
the new application (green) instead of the old one when verified.

Blue/Green deployments can prove costly due to the need to sustain twice the
amount of application resources for the duration of the deployment.

To start this, we set up a service that sits in front of deployments.

For example, the service selector section of the manifest file for a blue deployment 
for an app called web-app with v1.0.0 looks like this:

```
Type: Service
Metadata:
 Name: web-app-01
 Labels:
   App: Web-app
Selector:
   App: Web-app
   Version: v1.0.0
```
And the deployment for Blue Web App:

```
Type: Expansion
Metadata:
  Name: web-app-01
Specification:
  Template:
        Metadata:
           Labels:
             App: Web-app
             Version: "v1.0.0"
```
When we want to redirect traffic to the new (green) version of the app, 

we update the deployment file to point to the new version v2.0.0.

```
Type: Service
Metadata:
 Name: web-app-02
 Labels:
   App: Web-app
Selector:
   App: Web-app
   Version: v2.0.0
```
Expansion for Green App:

```
Type: Expansion
Metadata:
  Name: web-app-02
Specification:
  Template:
        Metadata:
           Labels:
             App: Web-app
             Version: "v2.0.0"
```

Thank you for reading my blog. If you like my work feel free to connect me on -> <a target = "_blank" href= "https://www.linkedin.com/in/krishnamohanyerrabilli"> LinkedIn </a> or <a target = "_blank" href= "https://www.twitter.com/K_Mohan_">Twitter</a>, see you with another one guys.  
