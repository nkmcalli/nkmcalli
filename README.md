<!---
nkmcalli/nkmcalli is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<h2>Testing table markdown</h2>

<table>
  <tr>
    <th>Test</th>
    <th>Test</th>
  </tr>
  <tr>
    <td markdown="span">`test` code style</td>
    <td>`test` code style</td>
  </tr>
  <tr>
    <td markdown="span">`test` code style</td>
    <td>`test` code style</td>
  </tr>
</table>

|Test|Test|
|-|-|
|`test` code style|`test` code style|
|`test` code style|`test` code style|
|`AbcdefghijklmnopqrstuvwxyzAbcdefghijklmnopqrstuvwxyz(AbcdefghijklmnopqrstuvwxyzAbcdef)`|`AbcdefghijklmnopqrstuvwxyzAbcdefghijklmnopqrstuvwxyz(Abcdefghijklmnopqrstuvwxy)`|
|`BcdefghijklmnopqrstuvwxyzAbcdefghijklmnopqrstuvwxyz(AbcdefghijklmnopqrstuvwxyzAbcdef)`|`AbcdefghijklmnopqrstuvwxyzAbcdefghijklmnopqrstuvwxyz(Abcdefghijklmnopqrstuvwxy)`|
|`CdefghijklmnopqrstuvwxyzAbcdefghijklmnopqrstuvwxyz(AbcdefghijklmnopqrstuvwxyzAbcdef)`|`AbcdefghijklmnopqrstuvwxyzAbcdefghijklmnopqrstuvwxyz(Abcdefghijklmnopqrstuvwxy)`|
|`DefghijklmnopqrstuvwxyzAbcdefghijklmnopqrstuvwxyz(AbcdefghijklmnopqrstuvwxyzAbcdef)`|`AbcdefghijklmnopqrstuvwxyzAbcdefghijklmnopqrstuvwxyz(Abcdefghijklmnopqrstuvwxy)`|



<h2>Git Cheatsheet</h2>

[managing-your-personal-access-tokens](https://docs.github.com/en/enterprise-cloud@latest/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

```text
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git checkout main
git fetch upstream
git merge upstream/main
git push origin main


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git fetch --all --tags        
git checkout -b <new-branch-name> <tag-name>


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git checkout main
git pull
git fetch

git checkout <branch>
git rebase main
(merge conflicts) <<<<<<< HEAD
git add --all
git commit -a -m ""
git rebase --continue
git push --force-with-lease  (git push --force)


For a typical team workflow on a feature branch like test-1:
On test-1:
git fetch origin
git rebase origin/test-1 # integrate your colleague’s changes
git rebase origin/main # bring in main changes
git push --force-with-lease

This leaves test-1 containing: 
all main updates, your colleague’s commits, and your own commits, 
in a clean linear history, without losing anyone’s work. 
If your team dislikes rebase, use the same sequence 
but with merge in place of rebase and push normally.​


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git cherry-pick --edit -x fed7612b 
git cherry-pick --edit -x 093997a469f125ddc6d0c44eb7eefe1845fdb8c7

git cherry-pick --edit -x 8c2df308^..47c0d874
git cherry-pick <start-commit-hash>^..<end-commit-hash>

Start 8c2df308
End 47c0d874

git cherry-pick --continue

git revert <commit id>

git commit --amend  (opens editor)


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
<<<<<<< HEAD


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
GitLab: use ~~~ to delineate change suggestions so it won't conflict with code blocks


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
[pretty]
	nkm = %C(yellow) %h %C(green) [%as] %C(blue) (%cn) %C(white) %s

git log --pretty=nkm --max-count=5
git log --pretty=nkm --max-count=5 --graph


b32feded  [2025-05-14]  (Nicole McAllister)  Commit message


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git remote add kyle https://github.com/KyleZheng1284/nv-ingest-lib-mode.git
git fetch kyle

git checkout -b nkm/kyle-edit-1 kyle/fix/libmode-quiet-logging

make changes
commit changes

git push origin nkm/kyle-edit-1

go to the colleague's fork to request the pr


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git fetch
git branch -v -a
git checkout <branchname>

git checkout -b new-feature origin/new-feature

git push --force

git fetch origin
git reset --hard origin/main

git reset --hard 78d764a3


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
System: Git root \ gitconfig
Global: C:\Users\username\.gitconfig
Global: ~home/username/.gitconfig

git config --global core.editor "notepad"
git config --global -e
