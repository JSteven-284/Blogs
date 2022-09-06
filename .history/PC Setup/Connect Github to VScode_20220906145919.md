## **Connect Github to VScode**
<br>

*This is the basic steps for setting up ssh key and connecting Github to local VScode.*
<br>
<br>


### **Step 1: Git installation**
<br>

Firstly, we need to install Git.  

More details are provided here:  
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git  
<br>

### **Step 2: Git Configure**  
<br>

Next, we need to use Git bash to set our username and email.  

Open Git Bash, and use these two lines for configuration with your preferred username and useremail:
```Bash
git config --global user.name "username"
git config --global user.email "useremail"
```
  
### **Step 3: Generate ssh key**  
<br>

Now we need to use Git bash to generate ssh key pair.  

Still in Git Bash, use the following line to generate a new ssh key:  
```Bash
ssh-keygen -t rsa -b 4096 -C "YOUR_GITHUB_EMAIL_ADDRESS"
```
Or, if we want to use ssh keys we already have, check them using:
```Bash
ls -al ~/.ssh
```

### ****