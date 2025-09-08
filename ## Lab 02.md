## Lab 02

- Name: Evan Hallmark
- Email: hallmark.5@wright.edu

## Part 1 Answers

Full / absolute path to your private key file: ssh -i "C:\Users\yraa5\OneDrive\2350 lab stuff\keys\labsuser.pem" ubuntu@54.208.254.90 

Command to SSH to AWS instance: 
```
[Place your ssh command here]
```

## Part 2 Answers

1. `chmod u+r bubbles.txt`
    - Means: allows the user to read bubbles.txt
    - Assessment: this is fine, the user can ONLY read bubbles.txt, if they are not the owner of the file, they cannot write nor execute the file but can read the contents of bubbles.txt.
2. `chmod u=rw,g-w,o-x banana.cabana`
    - Means: the user can read and write 
    - Assessment:
3. `chmod a=w snow.md`
    - Means: 
    - Assessment:
4. `chmod 751 program`
    - Means: 
    - Assessment:
5. `chmod -R ug+w share`
    - Means: 
    - Assessment:

## Part 3 Answers

1. Command to create new user: sudo adduser ehallmark (ehallmark is my replacement of `bob`)
2. Path to new user's home directory: /home/ubuntu ehallmark
3. Evaluate if `ubuntu` can add files to new user's home directory: no; if you use chown [new user] [file], the operation is not permitted for the ubuntu user.
4. Command to switch to new user: (sudo) su ehallmark (sudo is technically optional here)
5. Command(s) to go to new user's home directory: echo $HOME ehallmark
6. Evaluate if new user can add files to user's home directory: no; the new user does not have the permission to make a new file in their own directory.
7. Command to return to `ubuntu` user: exit
8. Command to return to `ubuntu` home directory: cd ~

## Part 4 Answers

1. Command(s) to create group named `squad` and add members: sudo addgroup squad
2. Command(s) to add `ubuntu` & user to group `squad`: sudo usermod -a -G squad ubuntu, sudo usermod -a -G squad ehallmark // I used phoenixnap.com in order to find out how to add members to the group.
3. Command(s) to allow `squad` to view the `ubuntu` user's home directory contents: sudo chgrp squad /home/ubuntu // phoenixnap.com was also used for this question.
4. Command(s) to modify `share` to have group ownership of `squad`: sudo chgrp squad share // phoenixnap.com was also used for this question.
5. Describe your tests and commands with the user account: 
6. Describe the full set of permissions / settings that enable the user to make edits: 

## Part 5 Answers

For each, write the command used or answer the question posed.

1. Command(s) to make file using `sudo`: sudo touch madewithsudo.txt
2. Command(s) to make file with `root`: sudo su - (to get to the root user), touch madewithroot.txt
3. Describe / compare ownership and permissions of files: the root user has the permission to do anything while the ubuntu user has limited permissions and would have to use sudo to do any kind of permissions.
4. Which account can do what actions? (Type Y or N in columns)

Contents inside of `share`
| Account   | Can View  | Can Edit  | Can Change Permissions    |
| ---       | ---       | ---       | ---                       |
| `root`    |    Y       |     Y      |               Y            |
| `ubuntu`  |           |           |                           |
| `ehallmark`     |           |           |                           |

`madewithsudo.txt`
| Account   | Can View  | Can Edit  | Can Change Permissions    |
| ---       | ---       | ---       | ---                       |
| `root`    |    Y       |     Y      |       Y                    |
| `ubuntu`  |           |           |                           |
| `ehallmark`     |           |           |                           |

5. Command(s) to modify permissions: 
6. How to give user account `sudo`: 

## Citations

To add citations, provide the site and a summary of what it assisted you with.  If generative AI was used, include which generative AI system was used and what prompt(s) you fed it.
