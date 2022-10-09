```
apiVersion: v1
kind: Service
metadata:
name: ent <<=== this name is registered with the cluster DNS
spec:
selector:
app: web
ports:
...
