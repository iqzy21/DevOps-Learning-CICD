#CICD
#what is CICD
CI = continus integration CI is about integrating cold changed frequently 
if in a team and workiong on changhes instead of waiting for everyone to finish and merge 
CI allows you to intergrate chnges several times a day being able to catch errors quickly

CD = continues deployment or continues delivery 
with continues deployment every change that passes the production stage of the pipeline is automatically released to users
which means no more manual deployment 
with continues delivery once code is intergrated it needs to stay in a deployable state this part makes sure that software can be released reliably at any time 
CICD helpes teams work effiecently catch errors early and release updates quickly and saftley 

#Overview and Why we need CI/CD
CICD pipe line is a series of steps that happen once a change is commited 
rundown of pipeline
commirt change = changes are pushed to github e.g code
trigger build = the commit you pushed is triggered and sends an auto buld process
build = code is compiled and all dependencies are assembled and built
notify of buold outcome = once build is dont system notifies team wether build was successfull or failed
ru tests = automated test that ensure changes dont break exising functiinality
notify of test outcome = notifies team of test outcome 
deliver build to staging = if tets passes the build is delivered to a straging environment for further testing 
delpy to production = code is deployed to production environment where users can access it
<img width="670" height="156" alt="image" src="https://github.com/user-attachments/assets/d5e4254f-6e5e-4380-b201-a4f2c0bad4c1" />

why is cicd important 
fast delivery = automating the integration and deployment processes means we can deliver new features much faster
improved quality = by continusly testing and intergrating code we catch and fix bugs early
reduce risks = small incrementation a deployments leads to less risk as eerrors can be dealt with on a smaller scale
better collaberation = cicd encourages collaberation among team members everyones work is intgrated frequently 

<img width="675" height="191" alt="image" src="https://github.com/user-attachments/assets/2618664e-8e06-4ce5-9c28-f03761190422" />

#popular CICD tools 
🔧 Popular CI/CD Tools – Quick & Memorable
GitLab CI/CD

Built directly into GitLab

No extra tools needed if your code is already on GitLab

Clean YAML pipelines

Strong default security and permissions

Best for: Teams fully committed to GitLab

Jenkins

Open source and extremely powerful

Thousands of plugins → can do almost anything

Highly customizable, but complex to manage

Requires ongoing maintenance

Best for: Advanced teams needing full control

Memory tip: Powerful but high-maintenance

CircleCI

Cloud-based and very fast

Easy setup with GitHub & Bitbucket

Minimal configuration

Popular with startups

Best for: Small teams that want speed

Travis CI

GitHub-first CI/CD tool

Simple configuration

“Just works” experience

Less flexible than Jenkins

Best for: Simple projects and quick pipelines

GitHub Actions

Built straight into GitHub

Uses workflow YAML files

Huge marketplace of actions

Excellent for open-source projects

Best for: GitHub-centric workflows

Memory tip: Code + CI in one place

Cloud Provider Native CI/CD

AWS → CodePipeline, CodeBuild, CodeDeploy

Microsoft Azure → Azure DevOps Pipelines

Google Cloud Platform → Cloud Build

Deep integration with their cloud services

Ideal for cloud-native architectures

Best for: Teams already locked into one cloud

<img width="519" height="386" alt="image" src="https://github.com/user-attachments/assets/c19c2bfe-c7ac-4bc6-9026-e2c51c310802" />

#Role of CI/CD in DevOps
cicd is vital part of dev ops 
explenation of the infinity 
this is infinuity because its always continues 
CI
1st you have the continues intogration code build and test this means
developers wirte code and commit changes frequently to the version control systems such as github git lab ect 
code is autmatoilckly built and compiled correclty ensuring despendencies are in place

CD
tested code is released onto a staging or prod enviroment
application is deployed so users can access
code is then moonitored
then aautomated tests run to veryfy code had been updated and there is no bugs 

<img width="430" height="256" alt="image" src="https://github.com/user-attachments/assets/957604e1-55e6-460f-9a89-82e153478837" />

benefits of cicd
collaberation = encourages better colaberation among team members by intergrating each work and fosters responsibility
automation = automate builds tests and deployment processes reducing manual errors and freeing up time for developers
continues feedback = cicd provides continues feed back at certain stages which alert the dev of any bugs or issues 
consistency = by using automated pipelines cicd ensures processes are cionsistant and takes out the it works on my machine problem 

#CI/CD in DevOps Architecture
STAGE BREAK DOWN
1ST source controll 
thsi is where dev store and manage code tools with tools like github gitlab ect
source control allows multiple developers to work in the same project without conflicts maintininng a history of changes and a line of colleaberaruon 

2nd stage cicd
this is where automation testing building and delpying process happens
this stage ensures codge changes continuesly  are integrated tested  and deployed

3rd stage mponitoring
this stage involves continuesly monitoring the application to ensure it runs smoothly tools like prpomethies hrafana and elk are used for this
they help treack code to find any issues and log impoertant evens 

this feedback loop is cruicial for stable mantencence 

you can aways go back to previous stagers for example when an error needs to be fixed 
<img width="803" height="450" alt="image" src="https://github.com/user-attachments/assets/7a4611f5-43d3-4b79-bbe1-f733f8948214" />
