* hm_home

This repository contains TOML files for Harmonie experiments. 
Each branch defines an experiment.

## How to run an experiment 
### ecgate

```bash
export PATH=$PERM/julia-1.1.1/bin:$PATH   
export JULIA_DEPOT_PATH=$PERM/fars/jlpkg4harmonie 
```

```bash
Harmonie start <branchname>
```

## Worktrees
It is convenient to have a directory for each experiment.
E.g. on ecgate  

```bash 
mkdir $PERM/git
cd $PERM/git
git clone --bare git@github.com:roelstappers/hm_home.git 
```

Then create a worktree for <branch> in  $HOME/hm_home/<branch> by

```bash
cd $PERM/git
git worktree add $HOME/hm_home/<branch> <branch>
```









