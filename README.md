hacknightIdeas
==============
To submit ideas for future Rackspace UK Tech/Hack night please do a pull request with your thoughts.

help on git
==============

See https://help.github.com/articles/fork-a-repo#create-branches.

If you commit something to your master and then your pull request is rejected (for any number of reasons), your master and upstream's master will have different commits. A feature branch allows you to say "I'm going to try this out. It will land back in my master if my pull request is accepted. If its not, I can just walk away".

So my workflow is something like this:

+ Fork this repo 
+ $ git clone your own fork of this repo
+ $ git checkout -b newfeature
+ $ git status (it will see that you're on the `newfeature` branch)
+ < edit files>
+ $ git add file1 file2
+ $ git commit -m 'Made this cool feature'
+ $ git push origin newfeature
+ < go to github.com and send a Pull Request (PR) >
+ < its reviewed and accepted into master>
+ $ git checkout master (switching back to YOUR master)
+ $ git fetch upstream (upstream's master has new stuff, including your newfeature changes)
+ $ git merge upstream/master (now your master has your new code)
+ $ git push origin master (push your master back out to github)

Rinse, repeat.

Every single tech is a git noob at some point. Just start.
