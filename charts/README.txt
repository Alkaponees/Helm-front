Command for start frontend
1.minikube ssh docker pull alkaponees/web-frontend:v3
2.helm create frontend
3.Open directory frontend and click on right mouse button open with VS code 
4. In values.yaml enter our image name in line repository, tags="v3"  
5. In services.yaml targetPort=3000
6. In deployment.yaml containerPort=3000
7. exit from directory frontend and start command helm install front ./frontend
8. kubectl expose service front-frontend --type=NodePort --target-port=3000 --name front-exp
9. minikube service front-exp
10.Enjoy our web application!!!! 