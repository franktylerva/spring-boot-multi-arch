# Building with KPack

1. Create a Docker Registry Secret

    ```bash
    kubectl create secret docker-registry builder-secret --docker-server=https://index.docker.io/v1/ --docker-username=<username> --docker-password=<password> --docker-email=test@mail.com
    ```

2.  Install a ClusterStore

    ```
    kubectl apply -f store.yaml 
    ```

3.  Install a ClusterStack

    ```
    kubectl apply -f stack.yaml 
    ```

4.  Install a Builder

    ```
    kubectl apply -f builder.yaml 
    ```