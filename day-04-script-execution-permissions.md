# Day 04 - Script Execution Permission

## What I Did
- Commands practiced:
  - `ls -l script.sh`
  - `chmod u+x script.sh`

## What I Learned
- ls -l script.sh -> To see current permissions on a script file
- Use chmod to add execution permission.

## Challenges / Questions
- Question: explain me the stripes
- | Character | Meaning            |
| --------- | ------------------ |
| `r`       | read permission    |
| `w`       | write permission   |
| `x`       | execute permission |
| `-`       | no permission      |

| Position | Meaning                            |
| -------- | ---------------------------------- |
| 1        | File type                          |
| 2-4      | Owner permissions                  |
| 5-7      | Group permissions                  |
| 8-10     | Others (everyone else) permissions |

