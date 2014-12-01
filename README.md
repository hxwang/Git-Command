Command
---

### Basic Operation
- `git status`: show status
- `git add FILE_or_Folder`: add matched file to change list
- `git commit`: commit change list
- `git commit -a`: commit all changed files
- `git push`: push
- `git rm FILE`: untrack matched files, and also remove local copy
- `git rm FILE --cached`: untrack matched files, but keep the local copy

### Move a subfolder to new repository
- [Ref](https://help.github.com/articles/splitting-a-subfolder-out-into-a-new-repository/)
- Step1: clone the repository you want to split `git clone ORIGIN_REPO_URL FOLDER_NAME`
- Step2: split the subfolder from original repository, `git filter-branch --subdirectory-filter YOUR_SUB_FOLDERNAME -- --all`
- Step3: create new repository on git hub
- Step4: set remote to the new reposity, `git remote set-url origin NEW_REPO_URL`
- Step5: force push `git push -u origin master`

### Config Git
- cache credential (username and password), set the timeout value!
  - `git config --global credential.helper "cache --timeout=3600"`
