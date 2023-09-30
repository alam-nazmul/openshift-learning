# openshift-learning
OpenShift: A tool for manage container

### OC login
```
oc login -u system:admin
```

```
oc login -u developer -p developer
oc whoami -t
<token>
curl -k https://192.168.99.102:8443/oapi/v1/projects -H "Authorization: Bearer <token>"
```

### Display projects
```
oc get projects
```

### Check available usres on the system
```
oc get users
```

### Modify the user policy and permssion
```
oc adm policy add-cluster-role-to-user cluster-admin administrator cluster role "cluster-admin" added: "adminstrator"
```

