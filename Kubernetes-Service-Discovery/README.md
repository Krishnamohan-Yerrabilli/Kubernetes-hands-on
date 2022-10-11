```
apiVersion: v1
kind: Service
metadata:
name: testing <- this name is registered with the cluster DNS
spec:
selector:
app: web
ports:
...
