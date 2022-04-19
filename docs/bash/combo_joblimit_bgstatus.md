---
layout: default
title: Combine Background Exit Status and Job Limit
parent: Bash
---

Combining a joblimit and a status check
---------------------------------------

Please refer to [job_limit](./limitnumberofconcurrentjobs.md) and [background
exit status](./backgroundprocessexitstatus.md) for explanations.

```bash
#!/bin/bash

job_limit () {
    # Test for single positive integer input
    if (( $# == 1 )) && [[ $1 =~ ^[1-9][0-9]*$ ]]
    then

        # Check number of running jobs
        joblist=($(jobs -rp))

        # Loop to heck whether jobs are still running
        while (( ${#joblist[*]} >= $1 ))
        do

            # Wait for any job to finish
            command='wait '${joblist[0]}
            for job in ${joblist[@]:1}
            do
                command+=' || wait '$job
            done
            eval $command
            joblist=($(jobs -rp))

        done
    fi
}

# Some function that takes a long time to process
longprocess() {
        # Sleep up to 14 seconds
        sleep $((RANDOM % 15))
        # Randomly exit with 0 or 1
        exit $((RANDOM % 2))
}

indeces=()
pids=()
# Run five concurrent processes
for i in {1..10}; do
        ( longprocess ) &
    
        # store PID of process
        pids+=("$!")
        indeces+=("$i")

        job_limit 6
done

# Wait for all processes to finish, will take max 14s
# as it waits in order of launch, not order of finishing

for i in ${!pids[@]}; do
        if wait ${pids[$i]}; then
                echo "Process ${indeces[$i]}, ${pids[$i]} success"
        else
                echo "Process ${indeces[$i]}, ${pids[$i]} fail"
        fi
done
```