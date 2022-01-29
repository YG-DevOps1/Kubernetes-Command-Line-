kubectl version
kubectl version --short
kubectl cluster-info
kubectl get pods -n kube-system
kubectl get pods -n kube-system -o wide

kubectl annotate − It updates the annotation on a resource.

$kubectl annotate [--overwrite] (-f FILENAME | TYPE NAME) KEY_1=VAL_1 ...
KEY_N = VAL_N [--resource-version = version]
For example,

kubectl annotate pods tomcat description = 'my frontend'
kubectl api-versions − It prints the supported versions of API on the cluster.

$ kubectl api-version;
kubectl apply − It has the capability to configure a resource by file or stdin.

$ kubectl apply –f <filename>
kubectl attach − This attaches things to the running container.

$ kubectl attach <pod> –c <container>
$ kubectl attach 123456-7890 -c tomcat-conatiner
kubectl autoscale − This is used to auto scale pods which are defined such as Deployment, replica set, Replication Controller.

$ kubectl autoscale (-f FILENAME | TYPE NAME | TYPE/NAME) [--min = MINPODS] --
max = MAXPODS [--cpu-percent = CPU] [flags]
$ kubectl autoscale deployment foo --min = 2 --max = 10
kubectl cluster-info − It displays the cluster Info.

$ kubectl cluster-info
kubectl cluster-info dump − It dumps relevant information regarding cluster for debugging and diagnosis.

$ kubectl cluster-info dump
$ kubectl cluster-info dump --output-directory = /path/to/cluster-state
kubectl config − Modifies the kubeconfig file.

$ kubectl config <SUBCOMMAD>
$ kubectl config –-kubeconfig <String of File name>
kubectl config current-context − It displays the current context.

$ kubectl config current-context
#deploys the current context
kubectl config delete-cluster − Deletes the specified cluster from kubeconfig.

$ kubectl config delete-cluster <Cluster Name>
kubectl config delete-context − Deletes a specified context from kubeconfig.

$ kubectl config delete-context <Context Name>
kubectl config get-clusters − Displays cluster defined in the kubeconfig.

$ kubectl config get-cluster
$ kubectl config get-cluster <Cluser Name>
kubectl config get-contexts − Describes one or many contexts.

$ kubectl config get-context <Context Name>
kubectl config set-cluster − Sets the cluster entry in Kubernetes.

$ kubectl config set-cluster NAME [--server = server] [--certificateauthority =
path/to/certificate/authority] [--insecure-skip-tls-verify = true]
kubectl config set-context − Sets a context entry in kubernetes entrypoint.

$ kubectl config set-context NAME [--cluster = cluster_nickname] [--
user = user_nickname] [--namespace = namespace]
$ kubectl config set-context prod –user = vipin-mishra
kubectl config set-credentials − Sets a user entry in kubeconfig.

$ kubectl config set-credentials cluster-admin --username = vipin --
password = uXFGweU9l35qcif
kubectl config set − Sets an individual value in kubeconfig file.

$ kubectl config set PROPERTY_NAME PROPERTY_VALUE
kubectl config unset − It unsets a specific component in kubectl.

$ kubectl config unset PROPERTY_NAME PROPERTY_VALUE
kubectl config use-context − Sets the current context in kubectl file.

$ kubectl config use-context <Context Name>
kubectl config view

$ kubectl config view
$ kubectl config view –o jsonpath='{.users[?(@.name == "e2e")].user.password}'
kubectl cp − Copy files and directories to and from containers.

$ kubectl cp <Files from source> <Files to Destinatiion>
$ kubectl cp /tmp/foo <some-pod>:/tmp/bar -c <specific-container>
kubectl create − To create resource by filename of or stdin. To do this, JSON or YAML formats are accepted.

$ kubectl create –f <File Name>
$ cat <file name> | kubectl create –f -
In the same way, we can create multiple things as listed using the create command along with kubectl.


