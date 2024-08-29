# SIEM-LAb

<h1>SIEM Lab</h1>

 ### 

<h2>Description</h2>
In this project Ill be showing a basic understaning on collecting log and creating Alerets using elastic SIEM
<br />


<h2>Utilities Used</h2>

- <b>Kali linux</b> 
- <b>Virutalbox</b>

<h2>Environments Used </h2>

- <b>Linux</b> 

<h2>Program walk-through:</h2>

<p align="center">
first sign up for a free elastic account the trial should be good for 7 days

![elastic2 0 part 1](https://github.com/user-attachments/assets/bc969e2d-eddb-46f4-8947-8690aadd593c)

After you have signed up next step will be to create your first deployment. I usually leave everthing as is exccept for the region

![elastic2 0 part 2](https://github.com/user-attachments/assets/0e0adccd-1d38-4559-899d-dfaeefc81458)

The next step would be setup the kali VM I usally select 64bit and will be using vituralbox to launch the VM. 

![elastic2 0 part 3](https://github.com/user-attachments/assets/83e6d483-43d9-4760-b54c-55bcdb4a6b10)

![elastic2 0 part 23](https://github.com/user-attachments/assets/876d1624-eae0-415c-a3d3-c93d7ee4a400)


Now open up whatever virtual platform your running configure the propritate setting to launch the Kali VM that you just dowmloaded. Use Kali for both username and password to make it simple.

![elastic2 0 part 24](https://github.com/user-attachments/assets/e9dbb292-c6c0-4d57-a87d-2b4f2e90aa89)

side not make sure before you launch the VM to go advanced settings and set the copy and paste function to Bidrectional. you will need this function enabled later on.

![elastic2 0 part 25](https://github.com/user-attachments/assets/51751f5e-45c4-46c2-89a3-8a7215ab054d)

After getting your Kali VM setup and logged in go back to the ELastic deployment. got to the home page and then click Add Integrations at the bottom left corner.

![elastic2 0 part 4](https://github.com/user-attachments/assets/dcf37c20-ccaa-40f7-95f4-b50ae7f802bb)

Next step is to click on elastic defend

![elastic2 0 part 5](https://github.com/user-attachments/assets/d121bb4e-e11b-4032-a2cd-06f08d4d1f83)

Then click to install the elastic agent. After that copy that linux command to use for the VM

![elastic2 0 part 6](https://github.com/user-attachments/assets/9e3ba019-dab2-4b4f-9535-f4d0c61d6592)

Before you run the command got to your VM and just run a simple Ping to make your VM is connecting to the internet.

![elastic2 0 part 7](https://github.com/user-attachments/assets/c49b8460-b457-4167-a8c9-f9fd3e8b2f2b)

In your terminal paste that command that you copied earlier and run it through for it to install. It should say elastic agent has been sucessfully installed. you can run a command  sudo systemctl status elastic-agent.service to verify the installation.

![elastic2 0 part 8](https://github.com/user-attachments/assets/0fb8c790-3770-4973-8484-bfbefd829d61)

Next we will be generating some security events using Nmap. run the command sudo nmap ip to start generating some events. Then try out other commands such as sudo nmap -sS ip address and sudo nmap -sT ip address. these are used to detect open ports

![elastic2 0 part 10](https://github.com/user-attachments/assets/a29354e1-9312-409f-afff-f917ba40d7d4)

Now that we have created some events and generated data from Kali VM to the SIEM now we can query the logs. go back to your elastic page and in the top right go to Observability click logs then stream to view the logs you created.

![elastic2 0 part 11](https://github.com/user-attachments/assets/f1a89008-086c-46da-a376-0d61f971667c)

Now in the search bar type in process.args:"nmap" to search for the events using nmap
