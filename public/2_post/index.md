# Using Github & Bitbucket with Http Without Input User & Pass All The Time


![Step 1](/images/2-post/step-1.png)

Common practice in cloning and work around git is using SSH, but sometimes setup SSH is a daunting task and troublesome especially for beginner.
There is another way to work around git without using SSH that is using HTTPS. If you're stuck when setup SSH by facing error that you can't solve, I encourage you to use HTTPS, it's not a shame to use HTTPS just take it easy. This approach feels more straight to the point to setup and run git.

```console
foo@bar:~$ git init
foo@bar:~$ git remote add origin https://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@github.com/wildanoo/hugo_paper.git
foo@bar:~$ git remote -v
origin  https://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@github.com/wildanoo/hugo_paper.git (fetch)
origin  https://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@github.com/wildanoo/hugo_paper.git (push)

foo@bar:~$ git add .
foo@bar:~$ git commit -m "init hugo paper"
foo@bar:~$ git push --set-upstream origin master
```

By doing so
