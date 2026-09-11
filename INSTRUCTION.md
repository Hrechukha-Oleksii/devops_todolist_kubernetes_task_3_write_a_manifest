1. How to apply Namespace manifest.

Go to devops_todolist_kubernetes_task_3_write_a_manifest\.infrastructure directory:

    cd \.infrastructure

Create Namespace from namespace.yml manifest:

    kubectl apply -f namespace.yml


2. How to apply Busyboxplus manifest.

Go to devops_todolist_kubernetes_task_3_write_a_manifest\.infrastructure directory:

    cd \.infrastructure

Create Busyboxplus pod from busybox.yml manifest:

    kubectl apply -f busybox.yml


3. How to apply Todoapp manifest.

Go to devops_todolist_kubernetes_task_3_write_a_manifest\.infrastructure directory:

    cd \.infrastructure

Create Todoapp pod from todoapp-pod.yml manifest:

    kubectl apply -f todoapp-pod.yml


4. How to test ToDo application using the `port-forward` command.

    kubectl port-forward pod/todoapp-pod 8081:8080 -n todoapp


5. How to test the application using the `busyboxplus:curl` container.

Check ip all of pods in the namespace:

    kubectl get pods -n todoapp -o wide

Connect to busyboxplus container terminal:
    
    kubectl -n todoapp exec -it busyboxplus -- sh

Run curl command with todoapp-pod ip:

    curl 10.1.0.54