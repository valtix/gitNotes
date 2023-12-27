# For macOS Ventura

* enter into terminal: ssh-keygen -t ecdsa   # follow the prompt
* enter into terminal: eval "$(ssh-agent -s)"   # this starts the ssh-agent

* update your config file (~/.ssh/config) with the following:
    Host github.com
        AddKeysToAgent yes
        UseKeychain yes
        IdentityFile ~/.ssh/name_of_your_private_github_file


  # add the SSH public key to your account on GitHub
* ssh-add --apple-use-keychain ~/.ssh/name_of_your_private_ghithub_file




* For Linux

1. Generate a new key: 
    ```
        ssh-keygen -t ecdsa   # follow the prompt
    ```
- go to settings and click on "SSH and GPG keys"
- click on "New SSH key"
- enter the publick key that was generated from the first step above
- authenticate new SSH key by running the following in your terminal: ssh -T git@github.com
- make sure you follow the prompt
