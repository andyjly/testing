# Hello world!
- test1, failed, pushed with wrong e-mail
	- was able to push to correct github repos
- test 2 it worked!

## Instructions:
- to have 2nd github account working on same computer:
1. ssh-keygen -t rsa -C "your-email-address"
	- **IMPORTANT** make sure when prompted save file as something new e.g. `id_rsa_blahh` and I saved to '~/.ssh/id_rsa_blahhh`
2. got to github account and add a new ssh, you'll grab from your `id_rsa_blahh.pub`
3. Now within your ~/.ssh directory create a config file
    - below i'll show a sample config file

    ```
    #Default GitHub
    Host github.com
      HostName github.com
      User git
      IdentityFile ~/.ssh/id_rsa

    #New GitHub
    Host github-andyjly
      HostName github.com
      User git
      IdentityFile ~/.ssh/id_rsa_blahh

    ```
4. then let's try it out by creating a random directory and then 
    - `git init`
    - **IMPORTANT** what wasn't mentioned is that if you don't change your e-mail configs it will show default e-mail account defeating the purpose.
        - do `git config user.email "your email"`
    - make a random doc or readme then go `git commit -m "first commit"`
5. Let's now go to our new git account and create a new project directory e.g. "testing"
6. Now back in command line we do `git remote add origin git@github-andyjly:andyjly/testing.git`
7. `git push origin master` and now go to your new git website and should be updated with your new e-mail



