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
<br>

### **Step 4: Add ssh key to github**
<br>

Now it is time to add the generated ssh key to github.  

Copy the ssh key using this in Git Bash:
```Bash
clip < ~/.ssh/id_rsa.pub
```
Then, open github and go to settings, we can find "SSH and GPG keys" section in the sidebar.  

Click the green button "New ssh key" and paste the ssh key into it.  

Also, we can add a title in order to recognize it and organize ssh keys in the future.  

Check the setup using this in the Git Bash:
```Bash
ssh -T git@github.com
```
If we did everything right, there should be a feedback like:
```Bash
# Hi Username! You've successfully authenticated, but GitHub does not provide shell access.
```
<br>

### **Step 5: Clone repo in github to VScode**
<br>

Create a new repo or open an existing repo in github, copy the url by clicking the "Code" button.  

Open VScode, click "Source Code" in the sidebar and click "Clone a repo".  

Paste the url and choose a 