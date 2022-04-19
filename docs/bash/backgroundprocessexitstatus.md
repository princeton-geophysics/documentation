---
layout: default
title: Background Job Exit Status
parent: Bash
---

# Save the exit status of background processes


```bash
    # Some function that takes a long time to process
    longprocess() {
            # Sleep up to 14 seconds
            sleep $((RANDOM % 15))
            # Randomly exit with 0 or 1
            exit $((RANDOM % 2))
    }

    pids=""
    # Run five concurrent processes
    for i in {1..5}; do
            ( longprocess ) &
            # store PID of process
            pids+=" $!"
    done

    # Wait for all processes to finish, will take max 14s
    # as it waits in order of launch, not order of finishing
    for p in $pids; do
            if wait $p; then
                    echo "Process $p success"
            else
                    echo "Process $p fail"
            fi
    done
```

**Note**: It should be noted that we can combine both the [job_limit](./limitnumberofconcurrentjobs.md) and the status check.
