# Instruction for me

1. ssh-keygen -t ed25519 -C "email@mail" или ssh-keygen -t rsa -b 4096 -C "email@mai"
2. ls -a ~/.ssh list keys
3. ssh -T git@github.com
4. git remote add origin git@github.com:<username>/<repo-name>.git
5. git remote -v


1. git init
2. git add --all
3. git commit -m "message"
4. git push -u origin master(main)


- git remote remove origin_name
- git remote rename oldname newname
- git remote show origin_name