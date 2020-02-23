# nodepublish
# Publishing packages to npm 

## Prerequisite
- git client installed to run commands through gitbash commandline tool to interact with git API.
- npm and node installed
- signed up to https://github.com/ repository
- signed up to https://www.npmjs.com/signup
- .npmrc is npm configuration file to define how npm should behave while running commands. This file would be available per user and available at c:/user/USER/.npmrc. By storing .npmrc file created per project helps to have different configuration for each project. .npmrc file to be placed in the root folder to be sibling of package.json or .gitignore files to be scoped for project.

## User Sample
To understand clearly the following example data would be used further for explanation;

Note: The example content is case sensitive
- Username is Drona
- Password is arjuna
- Email is Drona@somemail.com
- Repository name is photo-gallery
- Organization is drona

## Initial Setup
### NPM
- Login to https://www.npmjs.com
- Complete user account verification process.
- Click on avtar icon on top right and from the the drop down list select "Add Organization"
- In https://www.npmjs.com/org/create - Create new Organization page, enter a name in the field. For this example use "drona" which would create Org as @drona. This is referred under "name" key in package.json as an identifier to the package location. How this is added to package.json is explained later.
- Unlimited public packages
- Click on "Create" button under "Unlimited public packages (Free)"
- A link to Org page can be seen on the left side under Organizations section. For this example it would display as "drona".

### Git
- Login to https://github.com/
- Complete user account verification process.
- Create a new repository in https://github.com/drona?tab=repositories. To create one click on the "New" button on the right top in this page.
- Enter a repo name as "photo-gallery".
- Select "Public" which is for free but open for public access.
- Choose the option to create README.md file.
- Click on Create repository button to create a repository https://github.com/drona/photo-gallery

### Copy Git to local and make some changes
- From https://github.com/drona/photo-gallery click on "Clone or Download" button to copy https url of the git repository. This would look like https://github.com/drona/photo-gallery.git.
- Create a folder code and run gitbash from this folder.
- Run git clone https://github.com/drona/photo-gallery.git. This will copy the code from the repo into a new folder called "photo-gallery". 
- Run $ cd photo-gallery and move to newly created folder where the README.md file can be found.
- Run $ npm init to create package.json.
- When prompted for "name" enter "@drona/photo-gallery". It is very difficult to find unique name for a package as many packages would be creating with similar name. Org namespace @drona will help to differentiate package easily from other packages. 
- Remember that when published, this package will be added to npm under the org name specified in the package.json.
- When prompted to enter the repository type keep it as "git".
- When prompted to enter the repository url enter "https://github.com/drona/photo-gallery.git".
- Continue with rest of prompts to complete the creation of package.json.
- In case any of the details in package.json need to be modified that can be done at a later point too.
- Ensure .npmrc file is created under the root folder (under "photo-gallery" folder) if not already.
- .npmrc file which is npm configuration, should have an entry registry=https://registry.npmjs.org
- Make some changes to the code by adding some contents to README.md
- Push the changes from workspace to git repository (git add ., git commit -m "changes", git push origin master).

## Publishing Process
Login to npm account through command line.

$ npm login
> Username: Drona \n
> Password: arjuna \n
> Email: Drona@somemail.com

On successful login it will prompt that "Drona logged in to https://www.npmjs.com"

Run the command below to publish the package
$ npm publish --access public
Since it is public access (Unlimited free npm repo) --access public is required. On successful completion it will prompt + @drona/photo-gallery@1.0.0

The process to publish package is completed and can be imported to package.json of another project as "photo-gallery" : "1.0.0"

## Version Cutting
TODO







