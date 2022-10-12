
1. First, find the password.

```shell
git clone git@github.com:JayBeale/files-deleted-in-git-are-not-gone.git
cd files-deleted-in-git-are-not-gone
git reset --hard HEAD~1
cat password.txt
```

Then, try this yourself.

```shell
git clone git@github.com:JayBeale/files-deleted-in-git-are-not-gone.git
cd files-deleted-in-git-are-not-gone
echo "yourpassword" >password-2.txt
git add password-2.txt
git commit -m "initial password"
git push
git rm password-2.txt
git commit -m "deletion"
git push
echo "oh noes! The password is gone.  Can we get it back?"
git reset --hard HEAD~1
cat password-2.txt
```
