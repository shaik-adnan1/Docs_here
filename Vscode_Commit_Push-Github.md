Hello there, after forgetting many times on how to push new folders and files into github directly from the terminal using Vscode. 🥲😂
I hope it is finally time to create a simple yet useful process documentation.

As time goes on, I'll add steps for pulling requests, merging, and other related tasks.

Let's get this party started!

😶‍🌫️

Heading: Using Terminal (Vscode) to initialise, commit, and push code to github!!

 Navigate to the root directory of project folder in terminal and run 
 
1 =>"git init"

---- This will initialize and empty git repo in your project folder, that will basically keep track and update the files to GH..
Note: now you might notice a green letter saying "U" at the end of files: that is basically the "Untracked" files and those that haven't been commited yet!

2 => "git status"

---- This command will print the "Untracked" files to the terminal

3 => 'git add .'

----- This will add all the untracked files and make them ready to be commited!
Note: the period after add represents "add all untracked files". you can also add only desired files by running "git add <filename>"
-> Since the untracked files are now added, they are marked with green "A"

Extra => 'git reset .'
 
----- you can reset the added files back to untracked, if there weren't any permenant changes made to the files!

4 => 'git commit -m "<commit messege>"'
 
----- Now you can commit the added files that no longer taking changes currently, with  the above command ! 4 ! 
Note: the commit messege can be anything that describes the commiting files.. 
-> the "-m" means messege!! 

Extra => 'git log'
 
----- this will give the ID and basic info about the last commit!!
Note: after commiting if any changes are made to the files before pushing them, That file will be marked with an "M" which means modified!

Here's a shortcut: 

To directly add and commit the files at the same time you can use the following command

=> 'git commit -a -m "<commit messege>"'
easy peasy

Now create a new repository in github where you want these files/folder to be uploaded!!
  
Getting back to terminal!!
  
5 => 'git remote'
  ----- This will show you which remote repository's linked to the local project,
        For now it should return you nothing, since we haven't linked any repo yett!!

6 => 'git remote add origin <url to the github repo>'
  ----- Congragulations your repo has been established with the local working directory!!🎉
  -- Now that we did it, let's celebrate by moving on to the next stepp

7 => 'git push origin master/main(to which branch the changes need to be pushed)'
 ---- This will push you code along with the changes to the connected repository!!
 
 
HAPPY CODING
















