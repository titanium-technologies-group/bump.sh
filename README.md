# bump.sh

```bash
#!/bin/bash
#    _                                _
#   | |                              | |
#   | |__  _   _ _ __ ___  _ __   ___| |__
#   | '_ \| | | | '_ ` _ \| '_ \ / __| '_ \
#   | |_) | |_| | | | | | | |_) |\__ \ | | |
#   |_.__/ \__,_|_| |_| |_| .__(_)___/_| |_|
#                         | |
#                         |_|
#                               by @rakshazi
```

* Collects changes from commit summaries between branches
* Generates file `CHANGELOG.md` with list of all changes
* Commits that file with commit summary `Release v<NEW_VERSION>`
* Creates new tag with release version and changes list as message
* Pushes commit with new tag and updated changelog
* Opens Gitlab Merge Request (url generated from origin url) with predefined title and branches in browser

**PLEASE**, use http://semver.org/

## Integration with git

```bash
sudo curl -o /usr/local/bin/git-bump -s https://raw.githubusercontent.com/titanium-codes/bump.sh/master/bin && sudo chmod +x /usr/local/bin/git-bump
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
