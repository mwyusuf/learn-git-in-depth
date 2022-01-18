# learn-git-in-depth
Course week one all about git
<br/>
<h2>What's git?</h2>

```
git is distributed version control system
```
<div>Git store thing all in a git object (blob), git store compressed data in a blob with metadata in header and generate this data use SHA1.</div>
<h2>Git Commit</h2>
<div>
  Commit is a give information in git any changes up to the current condition, it's a combination from previous commit.
  Most important in commit:
  <ul>
    <li>cant change this commit</li>
    <li>cant edit</li>
    <li>cant go back</li>
    <li>cant change the author</li>
    <li>cant change the date</li>
  </ul>
  <div>Because if u edit this commit is gonna have a new SHA1 and have different SHA1</div>
</div>
<h3>Commit example using tree</h3>
<ol>
  <li>
    <img src="https://user-images.githubusercontent.com/85268263/149650457-eac24bc8-aaca-4c27-8161-8417a2e80622.png" alt="img-example-commit" />
  </li>
  <li>
    <img src="https://user-images.githubusercontent.com/85268263/149650761-23291a18-01a1-48bc-8a81-641a4f25cbd0.png" alt="img-metadata-commit"/>
  </li>
</ol>
<h2>Git Areas</h2>
<div>
  Git have a 3 area:
  <ol>
    <li>
      <div><strong>Working Area</strong></div>
      <div>This file in local area or only in your device (untracked file), in there u can modify your content</div>
    </li>
    <li>
      <div><strong>Stagging Area</strong></div>
      <div>This area used for thats file are going to be part of the next commit. this area know change between current commit and next commit</div>
    </li>
    <li>
      <div><strong>Repository</strong></div>
      <div>This area contains all commits and contains all files you have committed in git</div>
    </li>
  </ol>
</div>
<h2>Stashing</h2>
<div>
  One more place to store ur code in git without u commit your code. 
  It's useful if you want to switch branches without committing first when you have written code
</div>
<div>Commands in git stash:</div>

1. Command for stashing your code

```sh
git stash
```

2. Command for how to show your list stash

```sh
git stash list
```

3. Command for how to show your list stash

```sh
git stash list
```

4. Command for show your content in your list stash

```sh
git stash show stash@{n}
```

5. Command for apply ur last stash

```sh
git stash apply
```

6. Command for apply ur specific stash

```sh
git stash apply stash@{n}
```

7. Command for stashing untracked files

```sh
git stash --include-untracked
```

8. Command for stashing all files

```sh
git stash --all
```

9. Command for delete last stashing and applying change

```sh
git stash pop
```

10. Command for delete last stash

```sh
git stash drop
```

11. Command for delete specific stash

```sh
git stash drop stash@{n}
```

12. Command for delete all stash

```sh
git stash clear
```

<h2>Branch</h2>
<div>
  Branch is a just pointer to a particular commit. and where u make a new commit.
</div>

It is best to try to name your branches as specific as possible, so not to confuse them with any others. There are many naming conventions out there for branches, but for this week simply try to name them off of a feature. To see all your branches:

```
git branch
```

As you can see, you have created your branch, but are not currently on it. To navigate onto it please:

```
git checkout new-branch
git branch
```

Now you can see you are on that branch. Go back to master and now we are going to delete `new-branch`.

```
git checkout master
git branch -d new-branch
git branch
```

As you can see, your branch is now gone.
<div>
  U can see all command with branch in <a href="https://git-scm.com/docs/git-branch">here.</a>
</div>

<h2>Tags</h2>
<div>Tags point to a commit but store additional information such as author, message and date. Thus tags are more useful to "tag" a specific version and the tag will then always stay on that version and usually not be changed</div>

```
% git checkout master    
Switched to branch 'master'

% git tag my-first-commit

% tree .git/refs        
.git/refs
├── heads
│   ├── master
│   └── new_branch
└── tags
    └── my-first-commit

2 directories, 3 files
```

<div>
  U can see all command with tag in <a href="https://git-scm.com/docs/tag">here.</a>
</div>

<h2>Merging and Fast Forward</h2>
<div>Merge many parent into one commit and became one</div>
<div><img src="https://user-images.githubusercontent.com/85268263/149847499-215bfec5-274f-4de5-a11e-ca9da571013d.png" /><div>
<div><img src="https://user-images.githubusercontent.com/85268263/149847553-57b7dfd5-3dd5-4c3d-ae0f-7a3a87e394db.png" /><div>
  
<h2>Useful Commit message</h2>
Try to make the message at commit as clear as possible, because if there is a bug we can easily track it down, for release note, good for reviewer code, rolling back, and associate with ticket/task
<h3>Example bad commit message</h3>
<img src="https://user-images.githubusercontent.com/85268263/149848310-e076616b-154a-41db-840d-e001a1a7cdb1.png" />
  
<h2>Git Checkout</h2>
Git checkout restore working tree files or switch branches. It changes HEAD to point to new branch, copy the commit snapshot to the staging area, and update the working area with the new branch contents. Basically replace/overwrite the working area with the version from the current staging area.
<div><img src="https://user-images.githubusercontent.com/85268263/149849232-670b782a-c72b-488f-bffb-cc82f2fcb4f5.png" /></div>
  
<h2>Git Clean</h2>
Git clean will clear your working area by deleting untracked files and cannot be undone.
U can see the command clean in <a href="https://git-scm.com/docs/git-clean">here</a>
  
<h2>Rebase</h2>
The point at which I branched to move to a new starting point. use rebase when between ur branch feature and ur branch master have diverged and you want a messy merged commit in our history. Rebase give a new commit history
<img src="https://user-images.githubusercontent.com/85268263/149866436-f5e9782d-b646-4e00-a978-953b05a94e83.png" />
U can see the command clean in <a href="https://git-scm.com/docs/git-rebase">here</a>

<h2>Git vs Github</h2>
Git open source version control software. While GitHub is the key for collaborating with other developer, GitHub is a tool built on top of git with easy to use interface.
<h3>Remote</h3>
Remote u can use command

  ```sh
  git clone <url_branch>
  ```
<img src="https://user-images.githubusercontent.com/85268263/149867979-9003d55e-7d74-4f48-abc7-551e1788a60d.png" />

<h3>Fork</h3>
Fork is a copy of a another git repo in your repo
<h3>Pull Request (PR)</h3>
Pull Request like a request permision to maintener git for like a i have a new feature or i fixing bug
<img src="https://user-images.githubusercontent.com/85268263/149871326-d6712706-d0f6-4daa-8364-273fc7d60f42.png" />



<a name="resources" id="resources"></a>
# RESOURCES

* Github branch commands: https://git-scm.com/docs/git-branch
* Github tag commands: https://git-scm.com/docs/git-tag
* Github clean commands: https://git-scm.com/docs/git-clean
* Github rebash commands: https://git-scm.com/docs/git-rebash
