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

