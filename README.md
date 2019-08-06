# hm_home

This repository contains TOML files for Harmonie experiments. 
Each branch defines an experiment (E.g see the cy43_3dvar_exp branch) 
Only two files are required (main.toml and domain.toml) and will be validated using json schema. 
Other toml files are optional and overwrite default settings.


## How to run an experiment 
### On ecgate

```bash
# in the future this will become  `module load Harmonie`
export PATH:/perm/ms/no/fars/julia-1.1.1/bin:$PATH   
export JULIA_DEPOT_PATH=/perm/ms/no/fars/jlpkg4harmonie
```

```bash
export HMHOME=https://github.com/roelstappers/hm_home.git
```

To run an experiment defined in <branchname> 

```bash
Harmonie start <branchname>
```

## Worktrees
It is convenient to have a seperate directory for each experiment on ecgate to make edit TOML files
This can achieve as.  

On ecgate  

```bash 
mkdir $PERM/git
cd $PERM/git
git clone --bare git@github.com:roelstappers/hm_home.git 
```

Then create a worktree for <branch> in  $HOME/hm_home/<branch> by

```bash
cd $PERM/git
git worktree add $HOME/hmhome/<branch> <branch>
```
Note `hmhome` instead of `hm_home` to avoid any possible conflicts with existing experiments

 





