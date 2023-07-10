![imagen](https://github.com/spsrc/kubernetes-hubs/assets/7033451/6c3d8fb2-b83f-411b-837a-4a496b6cb6e6)


# SPSRC Jupyter/Binder Hubs deployments at the SPSRC

The SPSRC JupyterHub/BinderHub Services Repository is a centralized collection of `YAML` files and Notebook services deployed at the SPSRC. This repository aims to gather and showcase a variety of JupyterHub services that have been implemented and customized to meet the specific needs of different projects, schools and workflows at the SPSRC. 

By sharing these services, we aim to promote collaboration, knowledge sharing, and the reusability of JupyterHub configurations within our organization. The repository serves as a valuable resource for SPSRC members to discover, contribute, and learn from the diverse range of JupyterHub services that have been successfully deployed within our environment.

## Jupyter Hub for IAA Users

🔡 Features:
- Access based on LDAP
- JupyterHub
- Basic Storage (for regular clusters) and Cinder Storage (for OpenStack deployment)

🚀 Deployment to the latest version:

```
helm repo add jupyterhub https://hub.jupyter.org/helm-chart/
helm repo update
helm install --create-namespace --namespace=jhub-iaa jhub-iaa jupyterhub/jupyterhub  --values iaa-hub/values.yaml
```

🚀🩹 Deployment to a specific version:

```
helm repo add jupyterhub https://hub.jupyter.org/helm-chart/
helm repo update
helm install --create-namespace --namespace=jhub-escape jhub-iaa jupyterhub/jupyterhub --version 2.0.0 --values iaa-hub/values.yaml
```


Verify deployment version:

```
helm list --namespace jhub-escape
NAME            NAMESPACE       REVISION        UPDATED                                 STATUS          CHART                   APP VERSION
jhub-iaa     jhub-iaa     1               2023-06-30 11:19:44.91132246 +0000 UTC  deployed        jupyterhub-2.0.0        3.0.0
```





## Jupyter Hub for ESCAPE Users 

Features:
- Access based on IAM
- JupyterHub
- Basic Storage (for regular clusters) and Cinder Storage (for OpenStack deployment)

🚀 Deployment to the latest version:

```
helm repo add jupyterhub https://hub.jupyter.org/helm-chart/
helm repo update
helm install --create-namespace --namespace=jhub-escape jhub-escape jupyterhub/jupyterhub  --values escape-hub/values.yaml
```

🚀🩹 Deployment to a specific version:

```
helm repo add jupyterhub https://hub.jupyter.org/helm-chart/
helm repo update
helm install --create-namespace --namespace=jhub-escape jhub-escape jupyterhub/jupyterhub --version 2.0.0 --values escape-hub/values.yaml
```


Verify deployment version:

```
helm list --namespace jhub-escape
NAME            NAMESPACE       REVISION        UPDATED                                 STATUS          CHART                   APP VERSION
jhub-escape     jhub-escape     1               2023-06-30 12:17:49.71132246 +0000 UTC  deployed        jupyterhub-2.0.0        3.0.0
```



## Jupyter Hub + BinderHub for Dask

Features:
- Access based on IAM 
- JupyterHub and BinderHub
- Basic Storage (for regular clusters) and Cinder Storage (for OpenStack deployment)

🚀 Deployment to the latest version:

```
helm repo add jupyterhub https://hub.jupyter.org/helm-chart/
helm repo update
helm install --create-namespace --namespace=jhub-daskhub jhub-daskhub jupyterhub/jupyterhub  --values dask-hub/values.yaml
```

🚀🩹 Deployment to a specific version:

```
helm repo add jupyterhub https://hub.jupyter.org/helm-chart/
helm repo update
helm install --create-namespace --namespace=jhub-daskhub jhub-daskhub jupyterhub/jupyterhub --version 2.0.0 --values dask-hub/values.yaml
```


Verify deployment version:

```
helm list --namespace jhub-escape
NAME            NAMESPACE       REVISION        UPDATED                                 STATUS          CHART                   APP VERSION
jhub-daskhub     jhub-daskhub     1               2023-06-30 12:17:49.71132246 +0000 UTC  deployed        jupyterhub-2.0.0        3.0.0
```



## Jupyter Hub for PYSNACKS 2023

Features:
- Access based on user+password
- JupyterHub
- Basic Storage (for regular clusters) and Cinder Storage (for OpenStack deployment)


## Jupyter Hub for PYSNACKS 2022

Features:
- Access based on user+password
- JupyterHub
- Basic Storage (for regular clusters) and Cinder Storage (for OpenStack deployment)

## Jupyter Hub for SOMACHINE 2021

Features:
- Access based on user+password
- JupyterHub
- Basic Storage (for regular clusters) and Cinder Storage (for OpenStack deployment)

## Jupyter Hub for SOSTAT 2021

Features:
- Access based on user+password
- JupyterHub
- Basic Storage (for regular clusters) and Cinder Storage (for OpenStack deployment)
