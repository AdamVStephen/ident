#!/usr/bin/env bash
# Pre-commit script to extract the previous git commit hash to a file.
# Solution posted by kolypto on stackoverflow.com Q 3442874
# Minor additions by Adam Stephen

targetFile=${1:-gitcommit.py}

set -e

commit=$(git log -1 --pretty="%H%n%ci")
commit_hash=$(echo "$commit"| head -1)
commit_date=$(echo "$commit"| head -2 | tail -1)

branch_name=$(git symbolic-ref -q HEAD)
branch_name=${branch_name##refs/heads/}
branch_name=${branch_name:-HEAD}

echo -e "previous_commit='$commit_hash\ndate='$commit_date'\nbranch='$branch_name'\n" > $targetFile
