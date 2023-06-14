# CA-S23-starter
To begin the project, the initial step is to create a repository for your team. To do this, follow the link provided in the document, and create or join your team. Once your team is created, a private repository will be generated for you to utilize as a means of collaborating with your colleagues and submitting your code. The repository will be created empty, and you should clone it and push your work onto it. It is important to note that the handouts may undergo minor modifications and updates throughout the various phases of the project. Therefore, it is advisable to set up multiple remotes on your local clones to keep abreast of the latest changes.

## Git
Once you have established your team and private repository, the next step is to push the necessary materials into the empty repository. Do not push into your empty repository before adding the starter repository as staff. This could raise conflicts when trying to push starter code to your repository. Only one member of the team should do this. To begin, clone your empty repository onto your computer using either ssh or https.
```
$ git clone git@github.com:Computer-Architecture-Spring-2023-SUT/mips-processor-<team_name>.git
$ cd mips-processor-<team_name>
```
You’ll also need to add the starter code as staff with the following command:
```
$ git remote add staff https://github.com/MohammadAli-Khodabandelou/CA-S23-starter.git
```
Then run the following command to retrieve contents:
```
$ git pull staff main
```
You can establish your team's private repo by pushing into it:
```
$ git push
```
Your repository is now set up and ready for you to begin developing your processor. Going forward, you can treat your repository as a single remote and continue with your usual workflow. To get any updates to the starter, simply run:
```
$ git pull staff main
```
