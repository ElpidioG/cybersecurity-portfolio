# File Permissions in Linux

## Overview
Simulated role as a security professional managing file and directory permissions in a Linux
environment for a research organization, with the goal of protecting sensitive research data
from unauthorized access.

## Objective
Review existing file and directory permissions, identify access control issues, and apply
appropriate authorization settings so that sensitive files are accessible only to the correct
users and groups.

## Tools & Skills Used
- Linux command line (`ls -la`, `chmod`)
- Symbolic permission notation (owner / group / other, read / write / execute)
- Access control / least-privilege principles

## Process
1. Used `ls -la` to list file and directory details, including hidden files, and interpreted the
   10-character permission string for each (file type, owner, group, other).
2. Removed write access for "others" on `project_k.txt` using `chmod o-w project_k.txt`, since
   the organization does not allow outside write access to any file.
3. Adjusted the hidden, archived file `.project_x.txt` so the owner and group could read it but
   not write to it, using `chmod u-w,g-w,g+r .project_x.txt`.
4. Restricted the `drafts` directory — which belongs to a single user — by removing the group's
   execute permission with `chmod g-x drafts`, so only the owning user could access its contents.

## Findings / Outcome
Tightened access on two files and one directory, removing unintended write access for others
and unintended execute/write access for the group, bringing permissions in line with a
least-privilege model for sensitive research data.

## Artifacts
- `File_permissions_in_Linux.pdf` — full write-up with terminal screenshots and explanations

## Notes
Based on a simulated Linux environment from Google Cybersecurity Professional Certificate
coursework. Usernames and hostnames shown are lab-generated and not representative of a
real system.
