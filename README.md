# nodepublish
test npm publishing

# User
username: ramakrishnankv
password: ****
email: ramakrishnankv@yahoo.com

registry=https://npm.pkg.github.com/ramakrishnankv
to me added in .npmrc file with the project scope which means the .npmrc file should be sibling of package.json or .gitignore, etc.

Create git repository and use git to clone the repo.
For eg: git@github.com:ramakrishnankv/nodepublish.git
command line: git remote add git@github.com:ramakrishnankv/nodepublish.git
test: git remote -v

Generate secret key to use git url
TODO



Authenticate by logging

$ npm login --registry=https://npm.pkg.github.com
> Username: USERNAME
Password: TOKEN
Email: ramakrishnankv@yahoo.com