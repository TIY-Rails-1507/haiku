# Haiku

This is a short lesson in handling merge conflicts in Git.

To do this we will all edit the same file, which may result in merge conflicts.

We will then have to resolve them.


### Tasks:

#### Step 1
Each person should clone this repo - do not fork it, only clone it.

On your local machine, open poem.txt and create a Haiku - there are no prizes so any 3 lines are good enough. 

Ref: https://www.youngwriters.co.uk/types-haiku-poem

Example:
```
The sky is so blue. 
The sun is so warm up high.
I love the summer.
```

The title of the Haiku is: **Interweb**


#### Step 2
Do a git add, and commit as usual.

Try to push this back to the repo.

You will probably get a message saying you need to get the latest version before you can push.

Do a pull and try to resolve any merge conflicts

Rules for merging
* You must keep at least one of the lines from your poem
* Must keep at least one of the lines from the version you pulled down


#### More details

When you try to do a push you will see:

```
$ git push origin master
To https://github.com/TIY-Rails-1507/haiku.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/TIY-Rails-1507/haiku.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```
This is because someone else has commited and pushed chages to the repo. 

The second last line suggests doing a git pull. 

This will also result in error messages:

```
git pull
remote: Counting objects: 6, done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), done.
From https://github.com/TIY-Rails-1507/haiku
   d4a438f..e9dae66  master     -> origin/master
Auto-merging poem.txt
CONFLICT (content): Merge conflict in poem.txt
Automatic merge failed; fix conflicts and then commit the result.
```

This explains that there is a merge conflict in ```poem.txt```.

Open that file and notice how the merge conflict is indicated. 

Resolve the conflict - remove all merge indicators and make the file be in the state you want to commit it.

Please follow the merge rules stated above and remember to save the file.

Use ```git status``` to see the latest changes.
Do a git add on ```poem.txt``` and then type ```git commit``` - do not add a message.

VIM will open, and this will have a default commit message stating that it is a merge.
Exit vim by pressing ```esc``` then ```wq``` ```enter```

Now you can do a push with ```git push origin master```


Have a look on GitHub to see if it looks as you expect...

Follow the prompts, shout if you get stuck...
