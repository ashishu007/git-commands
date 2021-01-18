# Creating/Maintaining Git repo using command line.

## Create a repository on GitHub using the GUI on its website.

Let the name of repo be ```myRepo```

This repo can be termed as ```remote```.

## Now Clone the repo to the local machine

```
git clone https://github.com/your_username/myRepo.git
```

### Alternatively

If you already have a directory on your local machine and want to connect with the GitHub repo, you can do like this -

Open the terminal inside the folder and initialize it with:

```
git init
```

This can be tered as ```local```.

### Synchronization

Now connect your ```local``` with ```remote``` by using this command:

```
git remote add origin https://github.com/your_username/myRepo.git
```

Then synchronize your ```local``` with ```remote``` by using this command:

```
git pull origin master --allow-unrelated-histories
```

Now your ```local``` code-base is synced with your ```remote``` GitHub repo.

These steps are required to be done once in the start only.

## Updating

The next three steps can be used to update your changes anytime.

    1. git add .
    2. git commit -m "some message"
    3. git push origin master

For a specific branch, change the third command as:

    3. git push origin branch_name

You can also clone an already existing/developed library using:

```
git clone https://github.com/repo_owners_username/repo_name.git
```

## To clone a specific branch, use:

```
git clone -b branch_name https://github.com/repo_owners_username/repo_name.git
```

## To delete a branch:

```
git push --delete origin branch_name
```

## To untrack the tracked changes:

```
git rm --cached . -r (This will untrcak all the changes)
```

## Get the remote url

```
git config --get remote.origin.url
```

## Change the remote url

```
git remote set-url origin new.git.url/here
```

## Change the local repo name

```
git branch -mv master main
    
git branch -mv old_name new_name
```
