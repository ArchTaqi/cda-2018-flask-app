# Deploy Flask App to AWS ECS Fargate


```shell
docker build -t cda-flask-app .
docker run -p 80:80 cda-flask-app

aws ecr create-repository --repository-name cda-penguin-app1123 --region eu-west-2 --profile archtaqi
aws ecr get-login-password --region eu-west-2 --profile archtaqi | docker login --username AWS --password-stdin ACCT_ID.dkr.ecr.eu-west-2.amazonaws.com

docker tag cda-flask-app:latest ACCT_ID.dkr.ecr.us-east-1.amazonaws.com/
docker push ACCT_ID.dkr.ecr.us-east-1.amazonaws.com/hello-world
```
