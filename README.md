# Task on GitHub Topic

1. Add user `softservedata` to this repository.

2. Create branch `develop` as default branch.

3. Protect branches `main` and `develop` with these rules:
- user can't merge to both branches without pull request
- allowed to merge to `develop` branch only if we have 2 approvals
- merge to `main` branch allowed if only owner approved PR
- assign the user `softservedata` as the code owner for all the files in the `main` branch
4. Add template (pull_request_template.md) to `.github` directory for creating issue in format:

## Describe your changes

## Issue ticket number and link

## Checklist before requesting a review
- [ ] I have performed a self-review of my code
- [ ] If it is a core feature, I have added thorough tests
- [ ] Do we need to implement analytics?
- [ ] Will this be part of a product update? If yes, please write one phrase about this update

5. Create project for this repository.

6. Add deploy key with name `DEPLOY_KEY` to your repository.

7. Create discord server and add notification when PR was created.

8. For github actions: 
- create PAT (Personal Access Token) with **Full control of private repositories** and **Full control of orgs and teams, read and write org projects**
- add to repository actions secrets key with the name `PAT` and the value of the created PAT

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

**Dillinger** is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |
