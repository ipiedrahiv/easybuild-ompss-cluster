# easybuild-ompss-cluster

## In order to run with UserInstallations module in DEEP

On an interactive session (salloc -p dp-cn -N 2 -n 48 -t 02:00:00 srun --pty --interactive /bin/bash):

1. Select a START_DIR = <...> (Ex. /p/scratch/deepsea/piedrahta-velez1/ompss2-eb-finaltest)
2. Create an easybuild install directory as EBINST_DIR = <START_DIR>/easybuild 
3. Export USERINSTALLATIONS

`export export USERINSTALLATIONS=<START_DIR>`

4. Load the UserInstallations module

`module load UserInstallations`

5. clone the repository into your easubuild install directory.

6. Run the easybuild command to install, give robot the absolute path to be safe.

`eb ompss2cluster-2023.11-gpsmpi-2022a.eb --robot=<EBINST_DIR>/easybuild-ompss-cluster`

## In order to test the installed software

1. Load the corresponding modules within an interactive session with UserInstallations module loaded with the same START_DIR

`module load module load Stages/2023  GCC/11.3.0  ParaStationMPI/5.7.1-1-mt nanoscluster`
`module load mcxxcluster`
