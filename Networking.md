# Google Cloud Platform (GCP): Networking, IPs and Domain Management

## ☞ _**Virtual Private Cloud**_

- ## Creating a VPC
  
    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP1.jpg" alt="GCP" width="600" />


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP2.jpg" width="600" />


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP3.jpg" width="600" />


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP8%20-%20successful%20VM%20creation.jpg" width="600" />



## ☞ _**IP Address**_

- ## Assigning a Dedicated IP address in GCP

    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP4%20-%20ubuntu.jpg" width="600" />


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP5.png" width="600" />


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP6.png" width="600" />


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP7%20-%20http%3Ahttps.jpg" width="600" />



## ☞ _**Mapping IP to a Domain**_

- (1) Using my stonybrook.edu email, I created a domain name through Namecheap: ‘raqs.me’
- (2) Copied the external IP address from my new GCP VM and added it while setting up a record in my domain through Namecheap.
  
    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP%20-%20copy%20ext%20IP%20address.jpg" width="600" />

  
    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP%20-%20namecheap.jpg" width="600" />

- (3) Created a new 'A' record on my domain through Namecheap.

    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP%20-%20create%20record%20-%20namecheap.jpg" width="600" />



## ☞ _**Deploying the Flask Application**_

  - Prior to creating a VM in GPC, I had already created a GitHub repository named `HHA504-flask-networking` and performed the necessary steps as demonstrated by my professor last week. These steps included creating a file named `app.py` that contains the commands or codes needed to complete this task and I utilized almost the same ones used by my professor, a `requirements.txt` file which contains the word 'flask’, and setting up a virtual environment. I tried to run the code, particularly testing port 5007 in a web browser. After these attempts, I proceeded to create a firewall rule.

## ☞ _**Creating a Firewall Rule and Configuring Firewall Settings**_
  
   <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP11%20-%20create%20firewall%20rule.jpg" width="600" />


   <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP12.jpg" width="500" />


   <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP13.jpg" width="500" />


   <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP14.jpg" width="400" />


   <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP15%20-%20successful%20creation%20of%20firewall%20rule.jpg" width="600" />


- (1) After clicking on the SSH, a new pop-up window or shell will appear where certain commands can be applied to successfully deploy the Flask application.
      
    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP16%20-%20for%20ssh.jpg" width="600" />

- (2) The photos below are from the new pop-up window (shell):
  
    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP17%20-%20pop-up1.jpg" width="600" />.


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP18%20-%20pop-up2.jpg" width="600" />.


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP19%20-%20pop-up3.png" width="600" />.


- (3) I copied the URL from my GitHub repository to clone the repository in the shell.
  
    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP20%20-%20copy%20github%20repo%20url.png" width="600" />.


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP21%20-%20git%20clone%20repo.jpg" width="600" />.


  *Initially, I ran into some error messages and `python3 app.py` wouldn’t work. However, after doing some research and encountering a similar error message in my other assignment for HHA 507, I tried the command `pip install flask`. This solution had worked for me previously in Visual Studio Code, and it worked successfully again, as shown in the photo.*

    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP22%20-%20python3%20app.py%20error%20%26%20soln.jpg" width="600" />.


    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP23%20-%20python3%20app.py%20error%20%26%20soln.jpg" width="600" />.


- (4) The changes I made in VSC were possible due to the `git pull` command. The port number changes are shown in the photo.
  
    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP25%20-%20git%20pull%20%26%20run%20app.py%20to%20see%20port%20changes.jpg" width="600" />.

- (5) I accessed my deployed Flask application using my `raqs.me` domain that I was able to configure. I made sure that the port number `5007` is also included in the URL. Photos below show how I searched for my domain using two different DNS checker websites. I ran into error messages before I was successful.
  
    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP26%20-%20dns%20look%20up.png" width="400" />.

    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP27%20-%20dns%20look%20up.png" width="400" />.
  
- (6) Before I successfully accessed my domain, I encountered error messages in the browser, similar to the issue shown in the recorded zoom class. However, after following the commands as taught by my professor, as shown in the first photo below, I was successful! See the last two photos.

    <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP29%20-%20sudo%20commands.png" width="600" />



## ☞ _**Successfully Deployed my Flask Application using GCP**_ 🙂

  - My `python.raqs.me` Domain + port number: 5007
    
      <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP30%20-%20successful%20(ip%20address).png" width="550" />

  - My IP address + port number: 5007
    
      <img src="https://github.com/raqssoriano/HHA504_NEW_assignment_networking/blob/main/GCP/GCP31%20-%20successful%20(raqs.me).png" width="550" />

  
