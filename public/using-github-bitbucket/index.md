# Using Http In Git Just Like SSH


Common practice in cloning and work around git is using SSH, but sometimes setup SSH is a daunting task and troublesome especially for beginner. There is another way to work around git without using SSH that is using HTTPS. If you're stuck when setup SSH by facing error that you can't solve, I encourage you to use HTTPS, it's not a shame to use HTTPS just take it easy. This approach feels more straight to the point to setup and run git.
As I know this method can be done in github and bitbucket since I already try both of it. For this example I will guide you using our lovely friend, github. 
First we have to set our Personal Access Token in github.

1. Go to your github and go to settings.
2. Select the developer settings
3. Open personal access token -> select Tokens (classic) -> Generate new token (Classic)

{{< figure src="images/step-4.jpg" title="Step 3" height="200px">}}

4. Set token name as you like

{{< figure src="images/step-5.jpg" title="Step 4" height="200px">}}

5. Check access that you want to give to the token and click generate token

{{< figure src="images/step-6.jpg" title="Step 5" height="200px">}}

6. Save the token since it will only show once.

{{< figure src="images/step-7.jpg" title="Step 6" height="200px">}}

7. Create new repository in your github and follow these steps to create new repo or push the existing one

{{< figure src="images/step-10.jpg" title="Step 7" height="200px">}}

And now the **final step** in our local repo. 

The example below is for project that does not have git in it. First initialize git in the project folder and setup the remote origin, add your generated token in the https link place it before github.com and add `@` after your token. 

For example if your https link is:
`https://github.com/wildanoo/hugo_paper.git`
and your personal access token is:
`ghp_QAxwhDxMu7aSxNM25vMmucalR6ybsD1wWYTU`

the remote url should be like this:
`https://ghp_QAxwhDxMu7aSxNM25vMmucalR6ybsD1wWYTU@github.com/wildanoo/hugo_paper.git`

Initialize git in your project folder and add the remote origin url

```console
foo@bar:~$ git init
foo@bar:~$ git remote add origin https://ghp_QAxwhDxMu7aSxNM25vMmucalR6ybsD1wWYTU@github.com/wildanoo/hugo_paper.git
```

You can check your remote url that you just add before.

```
foo@bar:~$ git remote -v
origin  https://ghp_QAxwhDxMu7aSxNM25vMmucalR6ybsD1wWYTU@github.com/wildanoo/hugo_paper.git (fetch)
origin  https://ghp_QAxwhDxMu7aSxNM25vMmucalR6ybsD1wWYTU@github.com/wildanoo/hugo_paper.git (push)
```

And now you can commit and push to your repo without always input username and pass, just like using SSH.

```
foo@bar:~$ git add .
foo@bar:~$ git commit -m "init hugo paper"
foo@bar:~$ git push --set-upstream origin master
```

Cheers! :beer::beer:
