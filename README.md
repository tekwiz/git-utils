# TekWiz's Git Utilities

Extra Git commands to make your life easier.

## `git-sync`

Synchronizes your current branch with the given remote:

    git sync origin
    
This is useful for ensuring proper synchronization of your branch with a common upstream, just
replace `origin` in the above command with the name of the common usptream remote.

Show usage information:

    git sync -h

## Git Flow commands

The git flow commands here are based on [A successful Git branching
model](http://nvie.com/posts/a-successful-git-branching-model/) by Vincent Driessen.  There is,
however, one significant difference regarding how release and hotfix branches are merged into
master and develop: instead of the branch being merged into master and develop separately, they
they are first merged into master, tagged, and then master is back-merged into develop.

### `git-flow-start`

Start a git-flow release or hotfix branch:

    git flow-start release 1.2.3

Replace `release` in the above command with `hotfix` to start a hotfix branch.

Show usage information:

    git flow-start -h

### `git-flow-finish`

Finish a git-flow release or hotfix branch:

    git flow-finish 1.2.3 release/1.2.3

If you omit `release/1.2.3` from the above command it would finish the current branch as v1.2.3.

## Copyright

Copyright 2016 Travis D. Warlick, Jr.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file
except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the
License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
either express or implied. See the License for the specific language governing
permissions and limitations under the License.
