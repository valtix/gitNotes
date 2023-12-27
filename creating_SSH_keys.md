# For macOS Ventura

* enter into terminal: ssh-keygen -t ecdsa   # follow the prompt
* enter into terminal: eval "$(ssh-agent -s)"   # this starts the ssh-agent

* update your config file (~/.ssh/config) with the following:
    Host github.com
        AddKeysToAgent yes
        UseKeychain yes
        IdentityFile ~/.ssh/name_of_your_private_github_file


- add the SSH public key to your account on GitHub
* ssh-add --apple-use-keychain ~/.ssh/name_of_your_private_ghithub_file




# For Linux

1. Generate a new key ( follow the prompt ): 
    ```
        ssh-keygen -t ecdsa
    ```
2. Start the ssh-agent in the background:
   ```
        eval (ssh-agent -c)
   ```
3. Add the your SSH key to the SSH-Agent:
    ```
        ssh-add ~/.ssh/id_ecdsa
   ```    
4. Go to settings and click on "SSH and GPG keys"
5. Click on "New SSH key"
6. Enter the public key that was generated from the first step above
7. Authenticate new SSH key by running the following in your terminal ( follow the prompt ):
    ```
        ssh -T git@github.com
    ```
