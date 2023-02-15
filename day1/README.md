1- Add bitnami helm chart repository in the controlplane node.

```helm repo add bitnami https://charts.bitnami.com/bitnami```

![add repo](images-result/lab1helm1.png)

2- Deploy the Apache application on the cluster using the apache from the bitnami repository. Set the release Name to: amaze-surf

``` helm install amaze-surf bitnami/apache ```

![install apache](images-result/lab1helm2.png)


3- Uninstall the apache chart release  from the cluster

``` helm uninstall amaze-surf ```

![uninstall apache](images-result/lab1helm3.png)

4- install specfic version of nginx 1.22.0, then update it to specfic 1.23.1, then rollback

```bash
helm search repo nginx --versions
helm install my-nginx bitnami/nginx --version 12.0.6
helm upgrade my-nginx bitnami/nginx --version 13.2.10
helm rollback my-nginx
```
![install nginx](images-result/lab1helm4.0.png)

![upgrade nginx](images-result/lab1helm4.1.png)

![rollback apache](images-result/lab1helm4.3.png)
