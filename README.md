# Instruction for me

1. ssh-keygen -t ed25519 -C "email@mail" или ssh-keygen -t rsa -b 4096 -C "email@mai"
2. ls -a ~/.ssh list keys
3. ssh -T git@github.com
4. git remote add origin git@github.com:"username"/"repo-name".git
5. git remote -v

---

1. git init
2. git add --all
3. git commit -m "message"
4. git push -u origin master(main) или другая ветка
5. git push --force грубо слить ветки с потерей непорядка

---

- git remote remove origin_name удалить оригин
- git remote rm origin_name удалить оригин v2
- git remote rename oldname newname
- git remote show origin_name

---

- git log
- git log --oneline
- git log --graph --oneline

---

- git status --ignored

---

- git commit --amend --no-edit добавить изменения к последнему коммиту и оставить сообщение прежним
- git commit --amend -m "edit commit message" изменить сообщение последнего коммита
- git restore --staged <file> переведёт файл из staged обратно в modified или untracked
- git reset --hard <commit hash> «откатит» историю до коммита с хешем <hash>. Более поздние коммиты потеряются!
- git restore <file> «откатит» изменения в файле до последней сохранённой (в коммите или в staging) версии

---

- git diff
- git diff --staged показать изменения, которые добавлены в staged-файлах
- git diff hash_a hash_b

---

- git clone git@github.com:"username"/"repo-name".git

---

- git branch список веток
- git branch -a список веток локальных и удаленных
- git branch "branch_name" добавить ветку
- git checkout "branch_name" переключить на ветку
- git checkout -b "branch_name" создать ветку и переключиться на нее

---

##разница веток

- git diff "branch_name_1" "branch_name_2" 
- git diff HEAD~ HEAD
- git diff HEAD~1 HEAD
- git diff hash~1 hash
- git diff master~3 master~1

---

- git merge main(master) объедини ветку main(master) с текущей активной веткой
- git merge --no-edit "branch" --no-edit избавляет от необходимости вводить сообщение для merge-коммита
- git branch -D "branch_name" жестко удалить ветку
- git branch -d "branch_name" удалить ветку если она является частью main

---

- git merge --no-ff "branch" отключить слияние веток Fast-forward
- git config [--global] merge.ff false отключить слияние веток Fast-forward навсегда

##.gitignore
- ** игнорировать все файлыв

- *.jpeg игнорировать все файлы, которые заканчиваются на .jpeg
- !doge.jpeg кроме этого файла
- docs/*/tmp игнорировать все файлы "tmp" во всех подпапках папки docs
- file?.txt fileA.txt file1.txt, но не file12.txt
- file[0-2][abc][a-z].txt игнорировать файлы file0.txt, file1.txt и file2.txt

- /todo.txt игнорировать todo.txt в корне репозитория
- spam.txt spam.txt будет игнорироваться во всех папках

- build/ игнорировать папку build

- docs/**/tmp игнорировать файлы docs/tmp docs/current/tmp, docs/old/tmp, а также docs/old/saved/a/b/c/d/tmp
- docs/*/tmp игнорировать только docs/current/tmp и docs/old/tmp