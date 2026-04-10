# AWS SAM Lambda Python S3 Example  
Lambda S3 Python lab from the Backspace Academy AWS Certified Developer Associate course.  

create virtual env in /code run -->

$ python3 -m venv v-env

This creates:

v-env/

  bin/
  
  lib/
  
  pyvenv.cfg
  
$ source v-env/bin/activate

now you will see (v-env) in front of command prompt -->

(v-env) ec2-user@...

now install pillow for images and boto3 for aws 

$ pip install pillow boto3

now we create the modules need for requirements.txt

$ pip freeze > requirements.txt

now we can deactivate virtual environment

$ deactivate

once env set we can use SAM using requirements.txt

$ pip install -r requirements.txt

$ sam build --use-container

$ sam deploy

if build fails for docker image -->
Trick Docker with a tag alias by pulling the correct image

$ docker pull public.ecr.aws/sam/build-python3.9:latest

Tag it with the name SAM expects -->
$ docker tag public.ecr.aws/sam/build-python3.9:latest public.ecr.aws/sam/build-python3.9:latest-x86_64

then build -->
sam build --use-container
