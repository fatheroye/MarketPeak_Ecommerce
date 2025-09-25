# Capstone Project: E-commerce Platform Deployment with Git, Linux, and AWS

## The Development of an e-commerce website for a new online marketplace  by name MarketPeak. 

# Tasks 1: Implement Version Control with Git

1.1. Initialize Git Repository: 


Create the project directory and name it "MarketPeak_Ecommerce". 

then cd into the new project directory and initialize a git repository.

mkdir MarketPeak_Ecommerce

cd MarketPeak_Ecommerce

git init

<img width="975" height="343" alt="image" src="https://github.com/user-attachments/assets/cb92d6a8-f351-43c2-96a4-f169a510d4bc" />


<img width="975" height="120" alt="image" src="https://github.com/user-attachments/assets/0c61c336-24ac-43ee-a03e-332ca5ff5dfc" />



1.2. Obtain and Prepare the E-Commerce Website Template:

1.3 Download a Website Template: 

1.4 Prepare the Website Template: 


<img width="1112" height="533" alt="image" src="https://github.com/user-attachments/assets/6c2efc53-5877-4c16-b7ba-000e2be6368c" />


1.5 Stage and Commit the Template to Git: I added the website files, setup Git configuration, and commit the changes to the MarketPeak_Ecommerce Git repository with the command


git add .


git config --global user.name "fatheroye"


git config --global user.email "oyebode171@yahoo.com"


git commit -m "Initial commit with basic e-commerce site structure"


<img width="975" height="322" alt="image" src="https://github.com/user-attachments/assets/e0bf0326-7346-4162-90e1-69f841d1163a" />
<img width="975" height="89" alt="image" src="https://github.com/user-attachments/assets/3e3e3590-ae32-47ad-9bba-190c9e44a9c3" />

1.6 Create a remote Github repository: I proceeded to create a repository on Github and named it Market_Peak_Ecommerce

<img width="975" height="472" alt="image" src="https://github.com/user-attachments/assets/88d8bf11-19bc-4928-8b92-513f4a455694" />




1.7 Link Local Repository to Github: On my terminal, i navigated to the project directory and cloned the remote repository URL to the local repository
git remote add origin https://github.com/fatheroye/MarketPeak_Ecommerce.git


1.7 Push the code to Github repository: I pushed the code using the following command
git push -u origin main

<img width="975" height="473" alt="image" src="https://github.com/user-attachments/assets/4c23e2cb-838c-4baf-8a6e-2263f87ea515" />

Step 2: AWS Deployment
Task 1: Setup an AWS EC2 instance for deployment
•	I logged in to the AWS Management Console.
•	I launched an EC2 instance using an Amazon Linux AMI.
•	I connected to the instance using SSH
•	I then proceeded to clone the Github repository to my AWS EC2 instance 

<img width="975" height="424" alt="image" src="https://github.com/user-attachments/assets/b7dd8c5f-d40e-45a6-8ec9-818658278a0f" />

<img width="975" height="457" alt="image" src="https://github.com/user-attachments/assets/b1647349-9bdd-4bc0-9609-85535ef838b3" />

<img width="975" height="319" alt="image" src="https://github.com/user-attachments/assets/44939079-6663-4564-b2c9-277bbf654a49" />


git clone git@github.com:fatheroye/MarketPeak_Ecommerce.git


<img width="975" height="487" alt="image" src="https://github.com/user-attachments/assets/05bfff66-c0fc-4378-8051-777772d8c88c" />


<img width="975" height="363" alt="image" src="https://github.com/user-attachments/assets/fb926c11-a123-4c1e-bb05-ba1811a985db" />


<img width="975" height="487" alt="image" src="https://github.com/user-attachments/assets/426b3f6a-4081-4916-901f-eab1b9f4b035" />


<img width="975" height="428" alt="image" src="https://github.com/user-attachments/assets/66d5300e-f069-4a84-95bc-a0de415ac436" />


Installing a web server on EC2**

Apache HTTP Server (httpd) is a widely used web server that serves HTML files over the internet. 


Installing it on Linux EC2 server will allow me to host the MarketPeak E-commerce site: Note that httpd is the software name for Apache on redhats systems using yum package manager
I then proceeded to install Apache web server on my EC2 instance using the following commands

sudo yum update -y

sudo yum install httpd -y

sudo systemctl start httpd

sudo systemctl enable httpd


<img width="975" height="432" alt="image" src="https://github.com/user-attachments/assets/ab04a3a8-2463-4502-9919-b46714ddc42e" />


<img width="975" height="478" alt="image" src="https://github.com/user-attachments/assets/93e84246-41cf-4f2d-bd0a-addf946c4b84" />

•	Prepare the web directory: 

I configured httpd for the website with the next command

•	sudo rm -rf /var/www/html/*

•	sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/


<img width="975" height="205" alt="image" src="https://github.com/user-attachments/assets/6cc4ca39-66c0-4d15-8202-168ffadb2f75" />

•	Reload httpd: I applied changes by reloading the httpd service

sudo systemctl reload httpd


<img width="975" height="484" alt="image" src="https://github.com/user-attachments/assets/db2440b4-a8f9-4bde-bbaa-673d5d1eca7f" />


<img width="975" height="485" alt="image" src="https://github.com/user-attachments/assets/173faeda-8795-4ba8-98b3-2a20c5fd0dcb" />





Access Website from Browser: 

After i configured httpd and website files intact, i proceeded to open my web browser to 

access MarketPeak_Ecommerce with the public IP of my EC2 instance. 


<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/5386d280-8cd6-4288-92f3-ee6c47f88efd" />

<img width="975" height="464" alt="image" src="https://github.com/user-attachments/assets/5736b864-de0b-4cb3-9bd1-fb4d033912a3" />


<img width="975" height="456" alt="image" src="https://github.com/user-attachments/assets/15e71434-ee59-49ef-8cc4-c462341e89c3" />


<img width="975" height="486" alt="image" src="https://github.com/user-attachments/assets/0b467949-8737-4b21-b6b8-531636038b90" />

<img width="975" height="478" alt="image" src="https://github.com/user-attachments/assets/76ae8ddc-fde1-46c7-8eb1-d7c4ac679865" />

<img width="975" height="469" alt="image" src="https://github.com/user-attachments/assets/c9119bf3-cf47-4f62-9822-44ec0a4ed3e4" />

Step 3: Continuous Integration and Deployment Workflow
To ensure a smooth workflow for developing, testing, and deploying my e-commerce platform, i created a seperate branch (Development branch).
git checkout -b development


<img width="975" height="137" alt="image" src="https://github.com/user-attachments/assets/229cfa24-807f-4978-a5f4-d7faf838e85b" />

Implement Changes: On the development branch, i added a new feature
Version control with Git: I used the following git command to stage, commit, and push to the development branch

git add .

git commit -m "Add new features or fix bugs"

git push origin development


<img width="975" height="323" alt="image" src="https://github.com/user-attachments/assets/f94c9c46-0e46-43cb-a522-260f66f83c5e" />


Pull Requests and Merge to the Main branch: I created a pull request to merge the development branch into the main branch from my remote Github. I then reviewed the changes for any potential issues. Then i proceeded to merge the pull request into the main branch.
git checkout main


git merge development


<img width="975" height="450" alt="image" src="https://github.com/user-attachments/assets/215c2d7b-e6de-452e-a7b9-6501531fc654" />

•	Push the Merged Changes to GitHub
git pull

git push origin main
•	Push the Merged Changes to GitHub
git pull

git push origin main



<img width="975" height="208" alt="image" src="https://github.com/user-attachments/assets/ac9672b3-3987-44f9-8040-05ab78bb3919" />

Deploying Updates to the Production Server: I pulled the latest changes on the server by opening my AWS EC2 instance where the production website is hosted, navigated to the website's directory and ran the following command
git pull origin main


•	I restarted the web server to apply the changes
sudo rm -rf /var/www/html/*
sudo cp -r ~/MarketPeak_Ecommerce/2137_barista_cafe/* /var/www/html/
sudo systemctl reload httpd


<img width="975" height="303" alt="image" src="https://github.com/user-attachments/assets/eb4b3b75-9e19-436d-a89e-ede706e55faf" />
