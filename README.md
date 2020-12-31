# Github - The Big Picture

 - Git is a version control tool
 - Git codebase is free and open-source software distributed under the terms of the GNU General Public License
 - Git is a distributed version-control system
 - Branches are lightweight
 - Strong support for non-linear development (thousands of parallel branches)
 - Nearly Every Operation Is Local
 - Maintains high integrity
 - Git Generally Only Adds Data
 
Most operations in Git need only locally files and resources to operate — generally no information is needed from another computer on your network. If you’re used to a CVCS where most operations have that network latency overhead, this aspect of Git will make you think that the gods of speed have blessed Git with unworldly powers. Because you have the entire history of the project right there on your local disk, most operations seem almost instantaneous.

Everything in Git is check summed before it is stored and is then referred to by that checksum. This means it’s impossible to change the contents of any file or directory without Git knowing about it. This functionality is built into Git at the lowest levels and is integral to its philosophy. You can’t lose information in transit or get file corruption without Git being able to detect it.

When you do actions in Git, nearly all of them only add data to the Git database. It is hard to get the system to do anything that is not undoable or to make it erase data in any way. As with any VCS, you can lose or mess up changes you haven’t committed yet, but after you commit a snapshot into Git, it is very difficult to lose, especially if you regularly push your database to another repository.

# Centralized Version Control System vs Distributed Version Control System

![cvcs-vs-dvcs](https://github.com/senthil-sekar/github-big-picture/blob/main/cvcs-vs-dvcs.png?raw=true)

In CVCS, the developer has a copy of the repository file system on his machine. So offline actions like commits (check-ins)  and seeing history are impossible since the local repository can’t save “changes”. 

DVCS means each developer has the entire repository, including the entire change history on his/her local machine. So the developer can see changeset history offline or commit (check-in) changes offline to his local repository.

# How Git stores the check-ins?

![git-check-ins](https://github.com/senthil-sekar/github-big-picture/blob/main/git-check-ins.png?raw=true)

# The Three States

![states](https://github.com/senthil-sekar/github-big-picture/blob/main/states.png?raw=true)

# Most common Git Commands

 - Clone - retrieve an entire repository from a hosted location via URL
 - Fetch - fetch down all the branches from that Git remote, but not merge yet
 - Checkout - switch to another branch and check it out into your working directory
 - Stage – stage the current version of your content for commit
 - Commit - commit your staged content as a new commit snapshot
 - Merge	 - merge the specified branch into the current one
 - Push - transmit local branch commits to the remote repository branch 
 - Pull - fetch and merge any commits from the tracking remote branch
 - Revert – a forward-moving undo operation
 
 # TFS Terminologies in Git World
 
- Main		    =>	Master
- Branch		  =>	Branch
- Map		      =>	Clone
- Check-out	  => 	Check-out
- Check-in 		=> 	Stage(optional), Commit, Push
- Undo		    =>	Undo
- Get Latest 	=>	Pull
- Merge		    => 	Merge
- Rollback		=>	Revert
- Code Review	=>	Pull Request

# TFS vs Git

![tfs-vs-git](https://github.com/senthil-sekar/github-big-picture/blob/main/tfs-vs-git.png?raw=true)

# Proposed Git Flow (Branching Strategy)

![git-flow](https://github.com/senthil-sekar/github-big-picture/blob/main/git-flow.png?raw=true)

- Develop branch is created from master
- Release branch is created from develop
- Feature branches are created from develop
- When a feature is complete, it is merged into the develop branch
- When ready for prod release, a release branch is created from develop branch
- When the release is done, the release branch is merged back into develop and master
- If any production issue, a hotfix branch is created from master
- Once the hotfix is complete, it is merged back into both develop and master

# Useful Links

 - Download Visual Studio Extension for Git from here https://visualstudio.github.com/
 - Learn more about Git here https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control
 - Download SourceTree from here https://www.sourcetreeapp.com/. This is the most popular Git GUI client to visualize the Git flow.
