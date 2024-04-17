# Agent setup 🕵️‍♂️

- Add an agent to the pool (In my case the agent is ruuning in ubuntu)<br/>
  ![agent running](assets/agent.png)<br/>
- Configure a self hosted agent<br/>
  ![agent config](assets/config.png)
  ![agent pool picture](assets/runningagent.png)<br/>

# Pipeline 🚀

My pipeline stored in _[YAML file](azure-pipelines.yml)_ :

- Starts on commit to main branch of the repository

- Installs dependencies

- Starts the application

- Runs a _[PowerShell script](tests/Powershell.Test.ps1)_ which tests the connection with the deployed application.

![alt text](assets/testing.png)

# Cases of Failure ⛔

Theese are examples of why the jobs might fail:

- Failure while installing the dependencies<br/>

![alt text](assets/startf.png)<br/>
![alt text](assets/installfcon.png)<br/>

- Failure while starting the application<br/>

![alt text](assets/startf.png)<br/>
![alt text](assets/startfcon.png)<br/>

- Failure While running the PowerShell script<br/>

![alt text](assets/pwshf.png)<br/>
![alt text](assets/pwshfcon.png)<br/>
