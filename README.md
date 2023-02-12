Thanks to .gitattributes, you can push your large files to Github.

### How to run LFS (Large File Storage)?

**Steps**:
1. Download the Git LFS file from [this address](https://git-lfs.com "this address") and install it on your computer.

2. Enable Git LFS by typing this command in the Git Bash screen. You only need to run this command once for each user account.
    
    `git lfs install`

3. You can run the file extensions that you want to be considered as large files one by one with this command.
 		
    `git lfs track "*<file>"`
 		
    Ex : `git lfs track "*.mp4"`

4. At this point, the .gitattributes file should have been created. Put the .gitattributes file in the root of your Unity project if not. If you are going to add too many file types, you can open the .gitattributes file with any text editor and add manually.

**Note**: If you are doing these operations after a push error, you may need to get a new commit.

Here is an example of a push from the first step with Git LFS:

    git init
    git lfs install
    git lfs track "*.mp4"
    git add template.mp4
    git commit -m "Example commit"
    git remote add origin https://github.com/exampleuser/example-project.git
    git push -u origin master

You can delete the shared file types you don't need. You don't have to use them all.
