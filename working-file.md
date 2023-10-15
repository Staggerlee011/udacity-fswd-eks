# working files

NOTE: endpoint only live during udacity project review

- test endpoint

``` bash
kubectl get services simple-jwt-api -o wide
export EXTERNAL_IP=a185d3deb589b415999c09c196defb78-1241672737.eu-west-2.elb.amazonaws.com/auth
```

- run auth endpoint

``` bash

``` bash
export TOKEN=`curl -d '{"email":"stebennettsjb@gmail.com","password":"myPassword"}' -H "Content-Type: application/json" -X POST a185d3deb589b415999c09c196defb78-1241672737.eu-west-2.elb.amazonaws.com/auth | jq -r '.token'`
```

- run content query

``` bash
curl --request GET 'a185d3deb589b415999c09c196defb78-1241672737.eu-west-2.elb.amazonaws.com/contents' -H "Authorization: Bearer ${TOKEN}" | jq 
```
