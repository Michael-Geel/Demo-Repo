# Demo

This is a basic repository I've created to learn how to use github.

This text was edited into the README after creation.

## Subheader

More text made in VS Code post clone.

When adding files to a project with git, need to use the "git add" command.
Will often see people typing: "git add ." This tells git to track all the files listed here, both untracked and modified files.
Note: Untracked means it's a new file that git doesn't recognize.
Alternatively, you can do "git add 'individual file name'" to add the individual files/folders by name you want it to track.

git status shows you the changes made to the git repo that are being tracked.
If all changes are being tracked and there's nothing showing untracked, then you can commit your changes to the repo.
Use "git commit -m "Insert message here."" to commit.
-Note -m is for message, as you need to have a message in order to commit your files.
-Generally the message should have something to do with the what and why behind the commit you're making.

With git commits, you can have 2 -m's in the commit line, the first -m is the commit "title", the second -m is the description.
Note git commit only saves the changes locally, the updates aren't live yet.
For that we need git push.

Going to commit here on this code, then will re-commit when time to push.

Use git push to send updates to the live environment repository where the project is hosted.
Attempting git push here failed. Need to learn the missing material necessary to successfully complete the push.

In order to push to GitHub under your account, you need to prove to GitHub that you're the owner of your account.
Have to connect local machine to GitHub account, and this is done using SSH keys.
Start by generating a SSH Key locally using the "ssh-keygen" command
You need to specify the type of encryption(-t), strength of encryption(-b), and finally at end include your GitHub email address.
The full command will look like this: ssh-keygen -t rsa -b 4096 -C "xy@domain.com"
It'll then ask for a file name with which to save the key, will default into your user folder/.ssh.id_rsa.
You can also provide a passphrase for your key (it is completely optional)
It'll generate to key files: file and file.pub.
-file.pub you upload to your GitHub interface. (pub = public, meaning it's your public key and is okay for others to see said key.)
-The file generated without .pub is your private key
You put your public key on GitHub, then every time you want to connect to GitHub or push your code or use account via local machine, use
your private key to show GitHub that you're the one the generated the public key.
View public key with command: cat "keyname".pub
Copy that entire key (from ssh-rsa to end of email address) Highlighting autocopies it as ctrl+c does something different in terminal.
Nav to GitHub and go to settings, select SSH and GPG keys and add the key there.
All that's left is to ensure then that your local git command line interface knows about the key you just generated.
-Note: open checking about starting ssh, there seems to be errors, however could generate a key in SSH, so will continue to run a push attempt.
May need to look at navigating through directories to the key.

For a git push, need two arguments: origin and master.
Origin identifies the location of our git repository and master is the branch we want to push to.

Have successfully pushed to live. Made following changes:
-On VPN
-Deleted old account credentials from windows managed accounts.
-Still hadn't successfully run the add key command. (Keys auto detected?)
-Created a new key to use.
-Set ssh to manually start via the services app.
-changed the "master" argument to "main" as it refers to the branch being pushed to.

Attempting to push once more to confirm all is a success (will attemp without VPN)

Successfully pushed to GitHub. Issues resolved.

Pushes are still being made using old git account. Need to see how to swap accounts so that git activity is correctly recorded.

Attempt 1 to set account to new credentials.
Testing successful account change.

It appears my account has successfully changed in git, however now my name is not showing up in github...?
-The commits do not appear under my account. No metric changes and no name.
-Will have to run this by Mat to see what's going on.

Confirming connection.

Opting to continue with the no-name issue present. Resuming Notes here starting from beginning of the "Git Push" portion of video.

For a git push, need two arguments: origin and master.
Origin identifies the location of our git repository and master is the branch we want to push to.
Master refers to the branch we're pushing to (will refer back to this.)

Will now look at creating a new repo locally.
See Demo-Repo2 for the continuation of the push notes.