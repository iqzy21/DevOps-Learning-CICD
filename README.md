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
fast delivery = automating the integration and deployment processes means we can deliver new features 
