# Class 6

## Notation for writing requirements

Name:
Description:
Actors:
Pre-condition: system state before starting use case
Post-condition: system state after completing use case
Main scenario: main use case flow
Alternative scenario: other possible flows, most often error handling

## Workflow modeling 

- Describes a system function in a business context (logic of events from a sequential perspective)
- Done with UML activity diagrams. Show the logic of events from a business perspective (not system perspective like in sequence diagrams)
- Elements:
    - Activity (rounded rectangle): an action or task
    - Control flow (arrow): shows the order of activities
    - Initial node (filled circle): starting point of workflow
    - Final node (filled circle with border): end point of workflow
    - Decision node (diamond): branching point based on conditions
    - Merge node (diamond): merging multiple flows into one
    - Fork node (thick horizontal/vertical bar): splitting flow into concurrent flows
    - Join node (thick horizontal/vertical bar): synchronizing concurrent flows into one

## Requirements validation

- Find issues with the derived requirements and iterate.
- Check for:
    - unambiguous / clear
    - realistic
    - necessary
    - quantifiable
    - testable
    - complete
- Why? Cost to fix bugs / problems grow exponentially with the project process
- How?
    - Reviews
    - Prototyping: build a prototype (model, simulation) and present it to stakeholders

## Version Control Systems

- Tools to manage changes to documents, programs, and other information stored as computer files
- Track changes + versions
- Branch out to collaborate

### Distributed VCS

        +----------------+
        | Central server |<--------------+
        +----------------+               |
            ^  |                         |
            |  v                         v
        +---------------+        +---------------+
        | Local copy 1  |        | Local copy 2  |<--+
        +---------------+        +---------------+   | integrate changes
        | Local changes |        | Local changes |---+
        +---------------+        +---------------+

- All local copies have everything from central server + more
- User modifies their local copy and merges modifications with central server
- For most operations, don't need connection central server
- Server crashes -> no problem since at least one local copy has everything

### Centralized VCS

- Single server stores all files + version history
- Users check out files from central server, make changes, and commit back to server
- No connection to central server -> can't do anything
- No local copy (always)

### Git

- Working tree: local files user is working on + .git directory (metadata + object database)
        
        .git/
        src/
        ...

- Snapshot: record of the state of the working tree at a given point in time (version of the code)
    1. Modify files in working tree
    2. Stage changes to be included in next snapshot
    3. Commit changes to make a new snapshot

- Commands:
    - git status: show status of working tree
    - git add <file>: stage file for next commit
    - git commit -m "message": commit staged changes with message (create snapshot)
    - git log: show commit history
    - git merge <branch>: merge branch into current branch
    - git push: send local commits to remote repository
    - git fetch: downloads data from the remote
    - git reset HEAD <file>: unstage file from next commit
    - git checkout HEAD: undo all changes to working directory and goes back to version at HEAD
    - git commit --amend: modify most recent commit (change message or add changes)
    - git revert <commit>: create new commit that undoes changes made in specified commit
    - git pull: fetch + merge changes from remote repository into current branch

- Branching:
    - develop in parallel without affecting main codebase
    - git branch <branch_name>: create new branch
    - git checkout <branch_name>: switch to branch
    - git merge <branch_name>: merge branch into current branch
    - Pull request: propose changes from one branch to be merged into another branch with GitHub (code review process)
    - Issue tracker: track bugs, tasks, feature requests
    - GitHub Projects: organize and prioritize work with Kanban boards