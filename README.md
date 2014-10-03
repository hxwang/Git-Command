Command
---

- `git status`: show status
- `git add FILE_or_Folder`: add matched file to change list
- `git commit`: commit change list
- `git commit -a`: commit all changed files
- `git push`: push
- `git rm FILE`: untrack matched files, and also remove local copy
- `git rm FILE --cached`: untrack matched files, but keep the local copy

### Move a subfolder to new repository
- [Ref](https://help.github.com/articles/splitting-a-subfolder-out-into-a-new-repository/)
- Step1: Clone the repository you want to split `git clone ORIGIN_REPO_URL FOLDER_NAME`
- Step2: Split the subfolder from original repository, `git filter-branch --subdirectory-filter YOUR_SUB_FOLDERNAME -- --all`
- Step3: Create new repository on git hub
- Step4: Set remote to the new reposity, `git remote set-url origin NEW_REPO_URL`
- Step5: Force push `git push -u origin master`
