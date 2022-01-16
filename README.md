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
