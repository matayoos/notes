## Thursday, March 4, 2021, 3:09:26PM -03 <1614881366>

### Working with branches

1. Show branches
  ```
  $ git branch
  ```

1. Create a new branch
  ```
  $ git checkout *-b* branch-name
  ```

1. Navigate into the named branch
  ```
  $ git checkout *branch-name*
  ```

1. Delete branch
  ```
  $ git checkout -d
  ```

1. Merge branches
  
  a. You can do using
  ```
  $ git merge
  ```

  b. but it is more common using
  ```
  $ git push -u origin branch-name
  ```

## Thursday, March 4, 2021, 3:06:19PM -03 <1614881179>

### Git add only modify files

- git commit *-am* "Message"

## Tuesday, March 2, 2021, 12:01:08PM -03 <1614697268>

### Git add only modify files

- git add -u

## Saturday, February 27, 2021, 5:13:50PM -03 <1614456830>

- git remote show origin

## How to delete commits from a branch

```
Return to the last commit

$ git reset --hard HEAD~

Return to a commit as you choose

$ git reset --hard <sha1-commit-id>

To reset your repo you must force push

$ git push origin HEAD --force
```
