# RevenueBySearchEngine
Install :
1. serverless  - 
    Install Node.js 6.x or later on your local machine
    Install the Serverless Framework open-source CLI version 1.47.0 or later

2. docker 

Settings :

IAM Role  - creation i am role with full admistration access
Github - Attach secret keys to github repos

3. Export IAM role acccess keys to local to test manually/locally
    serverless config credentials --provider aws --key AKIAW76GJRL7NC3GPXVY --secret +JK1Pqki9ULGQy2VH9ApJ49ygLlgmIT09VTG1lgC
Series of steps/commands 
------------------

1. > serverless create --template aws-python3 --path <your-path>
    handler.py
    .gitignore
    serverless.yaml

2. add python requirements
    requirements.txt
    > serverless plugin install -n serverless-python-requirements

3. Deploy Scripty
    Edit package.json to inclue serverless devdependencies and deploy script to use in github action
4. Deploy function manually (Docuker in local should be in running state)
    > npm run-script deploy

5. create github action 
    create .github/workflows/s3-to-lambda-deploy.yaml


Git commands :
---------------
git add .
git commit -m "add your comment"
git push


serverless plugin install -n serverless-python-requirements
npm run-script deploy

git add .
git commit -am "start"
git push