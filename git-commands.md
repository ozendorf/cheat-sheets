``` git config --global alias.stash 'stash --all' ```

``` git config --global alias.bb !better-branch.sh  ```

### conditional configs 
 ```
[includeIf "gitdir:~/projects/work/"]
  path = ~/projects/work/.gitconfig

[includeIf "gitdir:~/projects/oss/"] 
  path = ~/projects/oss/.gitconfig
 ```

### Blame
Showing authors of modified lines 
``` git blame -L 23,34 /path/to/file  ```

### Logs
Showing commit logs 
 ``` git logs -L 23,34:/path/to/file  ```

 
