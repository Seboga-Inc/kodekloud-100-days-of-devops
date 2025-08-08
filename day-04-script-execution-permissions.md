# Day 04 - Script Execution Permission

## What I Did
- Commands practiced:
  - `ls -l script.sh`
  - `chmod u+x script.sh`
  - './script.sh'

## What I Learned
- ls -l script.sh -> To see current permissions on a script file
- Use chmod to add execution permission.
- `-rw-r--r-- 1 user user 1234 Aug 8 12:34 script.sh` -> example
- ./script.sh -> to check the script is executable 

## Challenges / Questions
- Question: explain me the stripes
  
| Section | Characters | Meaning                              |
| ------- | ---------- | ------------------------------------ |
| Owner   | `rwx`      | Owner can read, write, execute       |
| Group   | `r-x`      | Group can read and execute, no write |
| Others  | `r--`      | Others can only read                 |


| Position | Meaning                            |
| -------- | ---------------------------------- |
| 1        | File type                          |
| 2-4      | Owner permissions                  |
| 5-7      | Group permissions                  |
| 8-10     | Others (everyone else) permissions |

