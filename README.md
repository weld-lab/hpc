# hpc
My scripts, personal notes & snippets to navigate an HPC environment

## Cheatsheet

### Environment Modules

- `module avail` : search for available modules
- `module load X` : load module `X` from the available list of modules
- `module unload X`: unload module `X` from the list of loaded modules 
- `module list` : list all loaded modules 
- `module purge` : unload all loaded modules

### Sun Grid Engine

SGE directives,

- `#$ -N myjob` : set the job name
- `#$ -pe X Y` : ask for `Y` (ex: 8)  cores of **p**arallel **e**nvironment `X` (ex: mpi, smp)
- `#$ -l h_rt=02:00:00` : walltime (ex: 2h)
- `#$ -cwd` : run job in current directory
- `#$ -j y` : merge `stdout` and `stderr`
- `#$ -o output.log` : redirect output to `output.log` file
- `#$ -M you@email` : email for notifications
- `#$ -m abe` : send mail at (**a**) start, (**b**) end, (**e**) error

Useful environment variables, 

- `$JOB_ID` : unique job identifier
- `$JOB_NAME` : job name
- `$NSLOTS` : number of allocated cores
- `$HOSTNAME` : compute node name
- `$QUEUE` : queue name
