# Create Personal Access Token on GitHub

From your GitHub account, go to **Settings** => **Developer Settings** => **Personal Access Token** => **Generate New Token** (Give your password) => **Fillup the boxes** => click **Generate token** => **Copy the generated Token**, it will be something like `ghp_sFhFsSHhTzMDreGRLjmks4Tzuzgthdvfsrta`
\
\
\
# Set This Token to Your Windows OS
Go to **Credential Manager** from **Control Panel** => **Windows Credentials** => find `git:https://github.com` => **Edit** => On Password replace with with your **GitHub Personal Access Token** => You are Done
\
\
If you don’t find `git:https://github.com` => Click on **Add a generic credential** => Internet address will be `git:https://github.com` and you need to type in your username and password will be your **GitHub Personal Access Token** => Click Ok and you are done
\
\
Now you can use this token while **git push** command as a password!
