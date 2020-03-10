
# [Google Cloud Shell](https://cloud.google.com/shell): 
It is a hidden germ that mostly goes under the rader. 
> Cloud Shell provides you with command-line access to your cloud resources directly from your browser. You can easily manage your projects and resources without having to install the Google Cloud SDK or other tools on your system. 

Some keys to take away
-  Google Shell is provisoned by e2-small Google Compute Engine
-  Limited storage 5G
-  But Google Cloud Shell is free for users with a Google Cloud Platform account.
-  It is secured
-  It has most of command line tools ( gcloud, mvn, git, ..) and text editors (nano, vim, emacs, etc) which are all that you need
-  It supports Java, Python, PhP, .NET, Go

# Starting Google Cloud Shell

- Option 1 - via Google Cloud Console
    - Open a webbrowser and visit http://console.cloud.google.com/ and switch to your project of choice
    - Click on the icon `\>` on top
    
- Option 2 - via Google Cloud Shell command line
    - Currently, this works only with `gcloud alpha`, so `gcloud component install alpha`
    - Then `gcloud cloud shell ssh --dry-run`, which shows which dry-runs the login
    - Then `gcloud cloud shell ssh` to start a Google Cloud Shell and login.
 
 # Installing Visual Code on Google Cloud Shell
 
 To do this, I am using > code-server is VS Code running on a remote server, accessible through the browser.
 `code-server` is available at https://github.com/cdr/code-server

 The first script named as `download_vs.sh` is to download a latest code-server binary 

  ```
  #!/bin/bash

  export VERSION=`curl -s https://api.github.com/repos/cdr/code-server/releases/latest | grep -oP '"name": "\K(.*)(?=")' | head -n 1`
  #wget https://github.com/cdr/code-server/releases/download//code-server-linux-x64.tar.gz
  wget https://github.com/cdr/code-server/releases/download/2.1698/code-server2.1698-vsc1.41.1-linux-x86_64.tar.gz
  tar -xvzf code-server2.1698-vsc1.41.1-linux-x86_64.tar.gz
  cd code-server2.1698-vsc1.41.1-linux-x86_64
  ```

  Then the second script named as `run_vs.sh` is to start Visual Code
  ```
  #!/bin/bash

  cd code-server2.1698-vsc1.41.1-linux-x86_64
  sudo ./code-server --no-auth --auth 'none' --port 8080
  ```

# Accessing Visual Code from a browser
