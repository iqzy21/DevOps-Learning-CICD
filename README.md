# CI/CD Learning Guide

## What is CI/CD?

### Continuous Integration (CI)
CI is about integrating code changes frequently. Instead of waiting for everyone on a team to finish their work before merging, CI allows you to integrate changes several times a day, enabling you to catch errors quickly.

**Key benefits:**
- Frequent code integration (multiple times per day)
- Early error detection
- Improved team collaboration

### Continuous Deployment/Delivery (CD)

**Continuous Deployment:** Every change that passes all production stages of the pipeline is automatically released to users. No manual deployment required.

**Continuous Delivery:** Once code is integrated, it stays in a deployable state. This ensures software can be released reliably at any time.

**Bottom line:** CI/CD helps teams work efficiently, catch errors early, and release updates quickly and safely.

---

## CI/CD Pipeline Overview

A CI/CD pipeline is a series of automated steps that happen once a change is committed.

### Pipeline Stages

1. **Commit Change** - Changes are pushed to version control (e.g., GitHub)
2. **Trigger Build** - The commit triggers an automated build process
3. **Build** - Code is compiled and dependencies are assembled
4. **Notify Build Outcome** - System notifies team whether build succeeded or failed
5. **Run Tests** - Automated tests ensure changes don't break existing functionality
6. **Notify Test Outcome** - Team is notified of test results
7. **Deliver to Staging** - If tests pass, build is delivered to staging environment
8. **Deploy to Production** - Code is deployed where users can access it

![CI/CD Pipeline Flow](https://github.com/user-attachments/assets/d5e4254f-6e5e-4380-b201-a4f2c0bad4c1)

### Why CI/CD is Important

- **Fast Delivery** - Automating integration and deployment delivers features faster
- **Improved Quality** - Continuous testing catches and fixes bugs early
- **Reduced Risk** - Small incremental deployments mean errors can be dealt with on a smaller scale
- **Better Collaboration** - Encourages teamwork as everyone's work is integrated frequently

![CI/CD Benefits](https://github.com/user-attachments/assets/2618664e-8e06-4ce5-9c28-f03761190422)

---

## Popular CI/CD Tools

### GitLab CI/CD
- Built directly into GitLab
- No extra tools needed if code is already on GitLab
- Clean YAML pipelines
- Strong default security and permissions
- **Best for:** Teams fully committed to GitLab

### Jenkins
- Open source and extremely powerful
- Thousands of plugins - can do almost anything
- Highly customizable but complex to manage
- Requires ongoing maintenance
- **Best for:** Advanced teams needing full control

### CircleCI
- Cloud-based and very fast
- Easy setup with GitHub & Bitbucket
- Minimal configuration
- **Best for:** Small teams that want speed

### Travis CI
- GitHub-first CI/CD tool
- Simple configuration
- "Just works" experience
- Less flexible than Jenkins
- **Best for:** Simple projects and quick pipelines

### GitHub Actions
- Built straight into GitHub
- Uses workflow YAML files
- Huge marketplace of actions
- Excellent for open-source projects
- **Best for:** GitHub-centric workflows

### Cloud Provider Native CI/CD
- **AWS:** CodePipeline, CodeBuild, CodeDeploy
- **Microsoft Azure:** Azure DevOps Pipelines
- **Google Cloud Platform:** Cloud Build
- Deep integration with cloud services
- **Best for:** Teams already locked into one cloud provider

![CI/CD Tools](https://github.com/user-attachments/assets/c19c2bfe-c7ac-4bc6-9026-e2c51c310802)

---

## Role of CI/CD in DevOps

CI/CD is a vital part of DevOps. The infinity loop represents the continuous nature of the process.

### The DevOps Infinity Loop

**Continuous Integration (CI):**
1. Developers write code and commit changes frequently to version control (GitHub, GitLab, etc.)
2. Code is automatically built and compiled, ensuring dependencies are in place
3. Automated tests run to verify code quality and catch bugs

**Continuous Deployment (CD):**
4. Tested code is released to staging or production environment
5. Application is deployed so users can access it
6. Code is monitored for issues
7. Feedback loops back to development

![DevOps Infinity Loop](https://github.com/user-attachments/assets/957604e1-55e6-460f-9a89-82e153478837)

### Benefits of CI/CD

- **Collaboration** - Encourages better teamwork by integrating everyone's work and fostering responsibility
- **Automation** - Automates builds, tests, and deployments, reducing manual errors and freeing up developer time
- **Continuous Feedback** - Provides feedback at certain stages, alerting developers to bugs or issues
- **Consistency** - Automated pipelines ensure consistent processes and eliminate "it works on my machine" problems

---

## CI/CD in DevOps Architecture

### Stage Breakdown

#### 1. Source Control
Where developers store and manage code using tools like GitHub, GitLab, etc.
- Allows multiple developers to work on the same project without conflicts
- Maintains a history of changes
- Provides a clear line of collaboration

#### 2. CI/CD
Where automation of testing, building, and deploying happens.
- Ensures code changes are continuously integrated, tested, and deployed

#### 3. Monitoring
Continuously monitors the application to ensure it runs smoothly.
- Tools: Prometheus, Grafana, ELK stack
- Tracks code to find issues
- Logs important events
- Provides crucial feedback loop for stable maintenance

**Note:** You can always go back to previous stages when errors need to be fixed.

![DevOps Architecture](https://github.com/user-attachments/assets/7a4611f5-43d3-4b79-bbe1-f733f8948214)

---

## GitHub Actions & CI/CD Workflow

### Workflow Process

1. **Write Code** - Fix bugs, develop features, etc.
2. **Commit to Repo** - Commit triggers a GitHub Actions workflow
3. **Workflow Definition** - Defined by a YAML file specifying actions to take on certain events
4. **Pipeline Starts** - Workflow enters CI pipeline
5. **Build** - Code is built and dependencies are installed
6. **Test** - Tests check that new code works with current state and ensure no bugs
7. **Check Test Outcome** - Crucial for maintaining code quality
8. **Package** - When tests and build pass, create a new deployment of your application

![GitHub Actions Workflow](https://github.com/user-attachments/assets/a7f8afca-3bf5-4d75-9f5a-540c0070e3f9)

---

## Use Cases for GitHub Actions

GitHub Actions can automate various aspects of development workflows:

### Continuous Integration
- Automatically builds and tests code every time it's pushed to the repo
- Ensures code is in good shape and catches issues early
- **Example:** Run unit tests on every pull request to ensure code doesn't break existing functionality

### Continuous Deployment
- After tests pass, automatically deploy updates
- Speeds up deployment by limiting manual intervention
- **Example:** Deploy an application to a cloud service after all tests pass for quick, reliable releases

### Automation
- Automate repetitive tasks in workflows
- **Example:** Manage project board automation, such as moving tasks on a GitHub project board

![GitHub Actions Use Cases](https://github.com/user-attachments/assets/0d80e746-f3a5-4e31-8d6e-0be082677d3c)

---

## Creating a GitHub Repo for CI/CD

![GitHub Repo Setup](https://github.com/user-attachments/assets/5a995271-4954-42a9-a1cd-6aac19a6c79e)

---

## Introduction to YAML Syntax

**YAML** = YAML Ain't Markup Language

A human-readable data serialization standard often used for configuration files in DevOps tools.

### Three Core Concepts

#### 1. Key-Value Pairs
Basic building blocks of YAML written as `key: value`

```yaml
name: iqzy
age: 30
job: dev
```

#### 2. Lists
Sequences of items using `-` to denote list items

```yaml
fruits:
  - apple
  - banana
  - cherry
```

#### 3. Nested Elements
Create hierarchies using indentation

```yaml
address:
  street: 12 Downing Street
  city: London
  country: UK
```

![YAML Syntax](https://github.com/user-attachments/assets/9bbff666-1385-4459-ba72-b1a711735c78)

---

## Workflow Syntax and Structure

### Key Components

- **name:** Name of your workflow
- **on:** Triggers the workflow on specific events (e.g., push, pull request)
- **jobs:** Tasks that run in the workflow
- **runs-on:** Environment where the workflow runs (e.g., `ubuntu-latest`)
- **steps:** Jobs are composed of steps - each step runs a command or action
- **actions:** Reusable code that can perform a variety of tasks

![Workflow Structure](https://github.com/user-attachments/assets/1fbd3d4a-3091-458a-a087-987f5dd29548)

---

## Events, Jobs, and Steps

### Events
Actions that trigger workflows (e.g., push, pull request)

### Jobs
- Independent tasks that run in parallel or sequentially
- Each job runs on a virtual machine

### Steps
- Individual commands or actions executed in a job
- Steps run sequentially within a job

![Events, Jobs, Steps](https://github.com/user-attachments/assets/46ebd3bd-a3ee-48b3-ba2f-ad22d90d6612)

---

## Building a Simple CI Pipeline

![Simple CI Pipeline](https://github.com/user-attachments/assets/cdbe5661-0fcf-4dfe-a626-79e8fbf623c2)

### CI/CD Demo Example

**Pipeline Configuration:**

![Pipeline Example](https://github.com/user-attachments/assets/1600a837-c696-47d3-8918-679b6ea8e789)

**In GitHub Actions:**

![GitHub Actions Result](https://github.com/user-attachments/assets/b463d7ba-89c4-46c7-b3ed-98bd60aa9a94)

---

## Advanced GitHub Actions

### Using Conditions and Expressions

**Conditions:** Allow you to control when a job or step should run based on certain criteria

**Expressions:** Provide a way to perform calculations, manipulate strings, and more within a workflow file

![Conditions Example](https://github.com/user-attachments/assets/b444648c-f526-4bf2-9348-577438ef7c1d)

### Matrix Builds and Parallel Testing

Matrix builds allow you to run multiple job configurations in parallel using the matrix strategy in GitHub Actions.

**Use case:** Testing across different environments simultaneously

![Matrix Build Example](https://github.com/user-attachments/assets/3f38e586-9917-4c03-838f-f9415a18a677)

#Secrets & Encrypted vars
secrets = are sensitive pieces off information such as API keys, passwords or any credentials that you dont want to be eposed int he dide base 
using secrets helps keep sensitive data secure out of the source code 

<img width="695" height="321" alt="image" src="https://github.com/user-attachments/assets/1dd47157-7014-4e3a-baf7-9f99371b7ad0" />
#Using secrets securely in workflow
two ways you can identify secrets
by using a echo function  as shown in the immage 
or a environment
<img width="672" height="250" alt="image" src="https://github.com/user-attachments/assets/dd95f78d-2a1f-48bb-8bf6-0bce1c0a8bee" />

#Reusable CI/CD
#Creating customs actions
custom actions are a way to automate parts of yourwork flow that are project specific 
they are reuasble peices fo code that automate specific tasjs in your CICD pipeline
3 types of actions 
javascript actions actions that use node js to run javascript code
docker actions for containers 
composite actions which are pieces that are reusable

cresating a cutom action 
create a repo to host custom axtion 
defien action meta data in an action.yml file
for example a javascript action would be writteen in a index.js  file
docker action would be wrotten in a docker file 
and composite actions would just use standard yaml

then you can publish action to github market place for open source use 
<img width="399" height="259" alt="image" src="https://github.com/user-attachments/assets/0ec36591-87ca-40d2-910b-4762eb33e486" />
<img width="329" height="243" alt="image" src="https://github.com/user-attachments/assets/e46a6fd3-05d0-4c86-bbf3-b09a74db47b7" />

#Sharing and reusing actions in diff projects
advantage if cusrtom action is being able to re use them it saves time and ensures consitancy across your pipelines 

reuasable actions help maintains consistancy across different reposetories as it has a standardised CICD ensuring processes and steps arew the same 
reduces error likley hood

reuasables help with effeciancy instead of rewiring actions you can re use the same one to save tiome 

example image 
<img width="344" height="337" alt="image" src="https://github.com/user-attachments/assets/c56cd078-55d3-4cd2-99b9-c7865499053e" />

cicd in the real world

# Automated testing and linting
liting is a process to analyse codde for potential errors and enforcing coding standards its liek havinga spell checker for your code checks for syntax bugs ect
benefits
you mainain code quality ensure code ahdiers to cioding standars making it easy to read and maintain
you can catch syntax errors early beforee they ebcome bigger probvlems
automated tests run autiomaticly on your code base to ensure irt works as expected 
tools for linting ESlint for javascript and pilot for python
benefits 
you can detect issues early such as bugs early in the dev process
it ensures code quality by consitantly running tests it ensures your code is relianable 
tools for automated testing you have j unit and py test jest and moicha 
<img width="855" height="455" alt="image" src="https://github.com/user-attachments/assets/fc481f2b-fe5f-4a2a-8dea-856c7bcc1ff4" />

#Deploying to different environments
environment types
whe working in an environment 3 or 4 of them are deployed development staging and production
development is where all the bulding and experementing happens it can be messy but that what development is about 
staging is a stable environment that mirrors production as closley as possible this is where final testing is done to catch final issues that got through deve;lopment
production is the live environemwnrt wherer the app is accessable to users this should be done cairuiflly and automated to avoid human error

deployment strategies 
2 types 
manual - moving code from 1 environment to another straight forward but prone to human erro and time consuiming 
automated -  where CICD shines uses scripts and tools to move code from 1 environment to anotther faster and more reliable liek a convair belt
cloud base tools to manage deploymentrs
AWS - EC2/ECS/EKS/lambda
AZURE - AKS/ app service 
GCP - cloud run/gke cloud functions/ app engine 
<img width="739" height="311" alt="image" src="https://github.com/user-attachments/assets/514608dd-37cc-4075-9cd5-5a206c021f09" />

# Security in CI/CD
as WORKFLOWS ARE AUTOMETED SECURITY IS NEED to protect cidee and data
BEST PRACTES 
secure secres such as API keys passwords and more use secrets in githuboir any other tool make sure its protected and not public in your code base
control access - control who has access to your repos and work dlows use permissions and role based access controll so the person witbh access can only do that 1 tasjk prevent accidental access
scan for vunrabilities - use tools like dependabot, snic or aother security cscanners that integrate with cicd pipe line by identify vunrabilities early yopu reduct a risk of securit breach
audit and monitor pipe lones for any unusual activity set notification for an changes inm your pipeline
<img width="712" height="310" alt="image" src="https://github.com/user-attachments/assets/08001817-77c6-4302-b160-5dcf86964dd3" />

#Debugging workflow failures
common for pipe line to dfail 
common isues 
failed test = it coild be your tets coukd gave faled for any reason look at ur code
dependency errors = these occure when when yiurt project relies on external libraries and packages that have conflicts and are not installed correctly
cobnfig werros = happewns wherre theres syntax errors like missing a space or indentatuon
permission issues = happes whern you dont have permission for a repositiry like accesuinfg secrets

solutins 
review loghs = logs give u more detaul a dninformation about the issue
re-run jobs = can deterimine if the falure was a fluke or a constant problkem 
update dependencies = ensure dependancies are up to dayte this can solve conflicts and compatability issues 
check config = make sure env variables and secrets are correctly set 
<img width="722" height="362" alt="image" src="https://github.com/user-attachments/assets/331864b4-bc08-4d15-a9d5-84501d8b4500" />

#Manual Triggers and Github actions
manual triggers allow wrok flows rto be started manually via github actions ui

used for certain deployments 
if you want to trigegr  deployments to various environments liek staging prod on diff times then you would use this 
for maintenence jobs such as data ,migration or data base back up you have this even for on demand jobs aswell 

example image 
in the immage you have the CI and as you can see after push there is manual commands for a dev to choose on what workflow to trigger and tets

<img width="434" height="390" alt="image" src="https://github.com/user-attachments/assets/69cb0bde-6040-46d0-94c8-2ca637ea791c" />
