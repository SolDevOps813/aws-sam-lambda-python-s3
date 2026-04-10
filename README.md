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

once env set we can use SAM using requirements.txt

pip install -r requirements.txt

sam build --use-container

sam deploy

