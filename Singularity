# Author: Shahzeb Siddiqui <shahzebmsiddiqui@gmail.com>

# docker-bootstrap:
# Copyright (c) 2015-2016, Gregory M. Kurtzer. All rights reserved.
# 
# "Singularity" Copyright (c) 2016, The Regents of the University of California,
# through Lawrence Berkeley National Laboratory (subject to receipt of any
# required approvals from the U.S. Dept. of Energy).  All rights reserved.

BootStrap: docker
From: shahzebsiddiqui/easybuild


%post

		su - easybuild
		export EASYBUILD_INSTALLPATH=/app
		export EASYBUILD_PREFIX=/scratch
		export EASYBUILD_TMPDIR=/scratch/tmp
		export EASYBUILD_MODULE_NAMING_SCHEME=HierarchicalMNS
		module use /app/modules/all/Core
 	        eb GCC-5.4.0-2.26.eb --robot
		exit 
 
%runscript
                eval "$@"

%environment
    source /etc/profile
    module use /app/modules/all/Core
    module load GCC/5.4.0-2.26


%label
AUTHOR Shahzeb Siddiqui <shahzebmsiddiqui@gmail.com>
