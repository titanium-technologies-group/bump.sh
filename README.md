# bump.sh

* Collects changes from commit summaries between branches
* Generates file `CHANGELOG` with list of all changes
* Commits that file with commit summary `Release v<NEW_VERSION>`
* Creates new tag with release version
* Pushes commit with new tag
* Opens Gitlab Merge Request (url generated from origin url) with predefined title, description and branches in browser

**PLEASE**, use http://semver.org/

## Integration with git

```bash
sudo curl -o /usr/local/bin/git-bump -s https://raw.githubusercontent.com/rakshazi/bump.sh/master/bin && sudo chmod +x /usr/local/bin/git-bump
git config --global alias.bump "git-bump"
```

## Usage

```bash
# Inside your repo
git bump <BRANCH_FROM> <BRANCH_TO>
```

`BRANCH_FROM` default: current branch

`BRANCH_TO` default: master

Just use:

```bash
git bump
```

And enjoy magic :)
