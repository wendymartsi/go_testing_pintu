
# Golang build with CI/CD

This repository contains the golang configuration, starting from the simple project, the pipeline and the manifest that will be executed for this project. This readme will also tell you how to use the repo to deploy to the cluster.


## Roadmap

- Install go package on local
- Create Project golang
- Using Jenkins
- Create job Jenkins
- Create Namespace on cluster
- Create pipeline
- Running Pipeline


## Tech Stack

**Client:** Golang, Jenkins

**Server:** Cluster

## Tutorial
1. Create go file main.go
2. Create Dockerfile on folder docker 
3. Create Jenkinsfile on folder pipeline 
4. Create job on jenkins 
5. Running jenkins job 
<img width="761" alt="Screen Shot 2022-11-16 at 22 11 15" src="https://user-images.githubusercontent.com/117815873/202218441-d048dcbd-cb3b-4f31-a9dc-99507fcd37c3.png">
6. Wait project running on cluster
7. Check pod on the cluster
```bash
  kubectl get pod -n staging
```
<img width="525" alt="Screen Shot 2022-11-16 at 22 12 17" src="https://user-images.githubusercontent.com/117815873/202218672-538b36fe-c0f4-4696-aca0-62e51533049b.png">
 
8. After running try to access the deployment to check make sure running
```bash
kubectl port-forward deployment/golang-simple -n testing 8080:8080
```
9. Access endpoint deployment
```bash
  localhost:8080 or localhost:8080/ping
```
<img width="339" alt="Screen Shot 2022-11-16 at 22 17 25" src="https://user-images.githubusercontent.com/117815873/202219984-969c8c11-80e2-4bca-9d44-c00815d89f83.png">
