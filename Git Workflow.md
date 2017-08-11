This document describes the official git workflow for SE. This is based on an earlier version by Laura who was inspired by a blog post which you might want to read too: [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/).

## The Official Git Workflow for SE Projects @RUG
The workflow we ask you to use assumes clear distinctions and roles for different branches of your version repository and code reviewing. 

### Master Branch
This is the branch you will use to hand in new versions of your application every two weeks. You will do this via a pull request, you have no other kind of access to this branch. The code of your pull request will be reviewed by you TA; after all their comments have been resolved, the pull request will be merged into the master.

### Develop Branch
This branch contains the current working version of your application. You still cannot merge to it, however you can send pull requests and ask one of your team members to review your code. After you have resolved their comments to their satisfaction your code will be merged into develop. It would be a good idea to add your TA as a reviewer as well  during the first weeks of the project so that you get a feel for what kind of feedback they are going to give. (See lecture #5 on Nestor for reviewing guidelines.)

### Feature Branches
Some properties of feature branches:
- They may branch off from develop.
- They must merge back into develop.
- They may have any descriptive name other than master, develop.
- They must be linked to a Trello card, GitHub issue, or any other issue tracking system that your team is using.

Creating a feature branch named myfeature.
```
git checkout -b myfeature develop
git push -u origin myfeature

```

Do some work on the branch.
```
git commit -am "some description of the small step you took.
```

Now, on GitHub you can send a pull request for the feature branch to be merged into develop by following the following steps:
1. Write a short description of what you did. You should be able to keep it short, since you shouldn't be implementing large changes in one branch. 
2. Request as reviewer someone from your team and your TA in the first weeks. Assign the reviewer to the pull request. 
Set the target branch, base branch on GitHub, of the pull request to develop.
3. The reviewer reviews and edits the code, the assignee creates and ships the code. 
Wait for the reviewer to review your code. If you have been asked to review code don't keep people waiting for days. 

### Release Branches
Some properties of release branches:
- They may branch off from develop.
- They must merge back into develop and master.
- They must be named release-*.
- They may not be used to add new features.

You 'll use these branches to prepare the code you are going to hand in at the end of your sprint, i.e. after two weeks. This branches should be used for last minute dotting of i’s and crossing t’s. Furthermore, they allow for minor bug fixes and preparing meta-data for a release (version number, build dates, etc.). By doing this work on a release branch instead of on the develop branch, part of the team can start working there for the next sprint. 

Creating a release branch named release-0.1.0:
```
git checkout -b release-0.1.0 develop
```

Do some work on the branch
```
git commit -am "Changed the version number in some file or something."
```

Send a pull request for the release branch to be merged into master. Do this via www.github.com
1. Request your TA as your reviewer.
2. Assign your TA to the pull request.
3. Set the base branch to master.

Send a pull request for the release branch to be merged into develop. Do this via the same process as merging a  feature branch.

After the release is merged into the develop branch tag it with the [correct version number](http://semver.org/):
```
git tag -a 0.1.0
```
