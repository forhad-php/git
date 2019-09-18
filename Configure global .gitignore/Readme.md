#### According to → https://medium.com/surabayadev/configure-global-gitignore-66a4e665c075

## First check whether it’s configure or not use command below:

`git config --get core.excludesfile`

## If your global not yet configure you can configure it using command:

`git config --global core.excludesfile C:\xampp\htdocs\.gitignore`

## Check again..

### Note: Why global .gitignore?

> For example you are using jetbrains IDE, jetbrain will create .idea folder in your root project folder. then you also use Netbeans IDE, Netbeans will also create folder with name .nbprojects. you always ignore these files in every single project you’re working on.

## Rename `gitignore.txt` to `.gitignore` and use it globally.
