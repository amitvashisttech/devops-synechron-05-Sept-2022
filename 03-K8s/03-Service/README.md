```
  128  cd 06-Service/

  129  ls
  130  cat helloworld.yaml 
  131  vim helloworld.yaml 
  132  kubectl  apply -f helloworld.yaml 
  133  kubectl  get deploy 
  134  kubectl  get svc 
  135  kubectl  delete svc helloworld-deployment
  136  ls
  137  kubectl  get deploy 
  138  kubectl  get pods 
  139  kubectl  expose deploy helloworld-deployment
  140  kubectl  get svc 
  141  curl 10.107.52.235
  142  kubectl edit svc helloworld-deployment
  143  kubectl  get svc 
  144  kubectl describe svc helloworld-deployment
  145  kubectl  get pods -o wide --show-labels
  146  kubectl describe svc helloworld-deployment
  147  kubectl  get pods --show-labels
  148  kubectl describe svc helloworld-deployment
  149  ls
  150  kubectl  get svc 
  151  kubectl  delete svc helloworld-deployment
  152  ls
  153  vim helloworld-svc.yaml
  154  kubectl  apply -f helloworld-svc.yaml 
  155  kubectl  get svc 
  156  kubectl describe svc helloworld-service
  157  ls
  158  cat app-svc-deployment.yaml 
  159  kubectl  apply -f app-svc-deployment.yaml 
  160  vim app-svc-deployment.yaml
  161  kubectl  apply -f app-svc-deployment.yaml 
  162  kubectl  get deploy,svc,pods 
  163  kubectl  get pods 
  164  kubectl  get deploy,svc,pods 
  165  kubectl  describe svc python-webapp-svc
  166  kubectl  get pods -o wide 
  167  kubectl  describe svc python-webapp-svc
  168  kubectl exec -it python-webapp-deployment-54b95bd8d-xgsdm -- sh 
  169  kubectl exec -it python-webapp-deployment-54b95bd8d-xgsdm 
  170  kubectl exec -it python-webapp-deployment-54b95bd8d-xgsdm -- cat app.py 
  171  kubectl logs  python-webapp-deployment-54b95bd8d-xgsdm
  172  vim /etc/hosts
```
