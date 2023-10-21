### Deploy model_example_a via `DREAM cli`, `kubectl cli` or `docker` 

__via DREAM cli__ 
Simple way to deploy to k8s


```
dream models deploy model_example_a v5
```


__via kubectl directly__
Direct way to deploy to k8s


```
git clone --branch v5 --single-branch git@github.com:dreamutherland/model_example_a.git
kubectl create namespace serve-model-model-example-a
kubectl create -f mlflow-serving.yaml
kubectl expose deployment model_example_a-deployment --port [PORT] --type="LoadBalancer"
```


__via docker (local)__
Local way to quickly test the image


```
docker run -d -p PORT:PORT jleighsutherland/model_example_a:v5
```


### Test "model_example_a" by executing `./infer.sh` 

__via infer.sh__ 


```
./infer.sh
```

