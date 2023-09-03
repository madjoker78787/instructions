# Instruction for me

1. ssh-keygen -t ed25519 -C "tixonov_igor@inbox.ru" или ssh-keygen -t rsa -b 4096 -C "tixonov_igor@inbox.ru"
2. ls -a ~/.ssh list keys
3. ssh -T git@github.com
4. git remote add origin https://github.com/<username>/<repo name>.git
5. git remote -v


1. git init
2. git add --all
3. git commit -m "message"
4. git push -u origin main
