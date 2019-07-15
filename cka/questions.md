# Certified Kubernetes Administrator Questions and Exercises

These are questions and exercises based around the CKA curriculum.

- For each section, the questions are intended to start easy and get more difficult while reinforcing the knowledge points in that section.
- Basic knowledge of pod creation or earlier sections may be required to complete a question.
- Questions are intentionally open to reinforce learning rather than copy and pasta
- There are no answers provided, in most cases, if you don't complete the task correctly then it won't work.
- It is assumed that you will be able to perform a quick ```kubectl get pod``` or ```kubectl describe pod <pod name>``` to validate exercise completion.

## 1.0 - Scheduling

### Labels and Label Selectors

1. Label a pod
2. Label a node
3. Schedule a pod to a node
4. View the labels on a pod
5. Schedule a pod to a node based on a built-in node label

### DaemonSets

1. Create a DaemonSet
2. Create a DaemonSet scheduled to a smaller subset of nodes

### Taints and Tolerations

1. Taint a node
2. Create a toleration such that a pod will be scheduled to a node it otherwise wouldn't be. A DaemonSet is good for this.
3. Create a toleration for a pod on against an automatic, node controller, applied taint
4. Create a toleration that will allow a pod to be scheduled on the master (not generally possible for cloud providers/managed Kubernetes)

## Cross skill questions and exercises

- Using a deployment with 4 replicas, limit all the replicas to one node, limit the deployment so that only pod will run due to resource limitations.