+++
title = 'Reinstall Problems'
date = 2023-11-26T14:11:14-06:00
draft = false
tags = ['debugging', 'story', 'git']
+++

## A Little Backstory...

After years of avoiding buying myself a MacBook, I finally succumbed to my own internal peer pressure and pulled the trigger. It was great. The m2 machines are fast, responsive, and easy to use. I got it all setup with brew, git, and all the other little tools that make a tinkerer’s life easier. I got it all stickered up and even took it with me on a trip to Europe. Everything was great in the world.

Then… disaster struck. As one gets older and one has carpal tunnel related issues, one can notice that they become more prone to dropping things. Or, maybe not, as I can attest. I did notice I was having problems holding things but I digress… I dropped an entire 750ml cup of water right onto the laptop. It was 3 months old and I just fried the logic board. I was devastated and I learned why people pay for AppleCare when the bill came due.

Why am I boring anyone reading this with the shortened version of my tale of woe? Well, because it leads right up to one of the major issues I dealt with in getting this very blog up and running in github and then on to netlify.

## Problem: Git No Work

I’ll cut right to the chase here, and I’m sure many people can relate to me on this one, but I was running into issues authenticating into git. No matter what I did, `git push` would not let me in. Alright, let’s start debugging.

### Is git installed?

First thing first, did I actually make sure git was installed and installed properly. Check, I had already installed Xcode and it came along for the journey. All the commands were responding appropriately and everything seemed fine.

### Did I generate a key?

Now is when the little story above starts to become relevant. I was sure I had authenticated myself to github and had an SSH key already registered with my account. I did it when I was setting things up, everything was ready, or so I thought. When I actually got down to looking, guess what? I was remembering from the original setup, before I had to have the logic board replaced. Alright, let’s try again. That had to be the problem, right? Let me generate a new key and all should be right with the world and… no, no it is not. I still can’t authenticate myself.

Well, maybe my machine and my local git are trying to log me in as my git user instead of the git user. Running a quick `ssh -T <username>@github.com` returned a promising “Permission denied (publickey).” I must be on the right trail! Let’s see if that’s the case by running one more command `ssh -T git@github.com`. Sadly, I was wrong again. That also returned a promising permission denied.

### gh auth

“What do I do now?”, I thought to myself. Oh, wait, I know! I’ll do what I always do when hitting problems. I’ll do a search. Stackoverflow and reddit quickly brought to my attention that I had failed to install the github cli and had not run the . As I was using github, this might be something I want to try. Did a quick install and typed in `gh auth login` without any hesitation. 

“What account would I like to log into?”

Well, I thought, I’m not special enough to have my blog on an enterprise github repo so I should pick GitHub.com. 

“What is your preferred protocol for Git operations?”

Ah ha! I know this one, ssh I selected with utmost confidence. But then, it wanted me to generate a new key and associate it with my account, but I had already done that and didn’t want to mess with multiple keys yet, so I quickly canceled out of that authentication prompt.

Back to the beginning, yes, plain old GitHub again, but this time I selected https. It prompted me to login, I did, and it returned a success. Will git push work this time? I crossed my fingers and typed out `git push -u origin main` and….. Success! It prompted me for my passphrase to access my key and I was in. I did it! I’m not just a schmuck anymore.


## Conclusion

Why did I bore any prospective audience with this? Well, apart from being able to get a fun story out of my misadventures, I wanted to remind everyone that even a senior developer can run into stupid basic issues. One is never too old or experienced to forget something taken for granted. Never forget how to debug an issue. Might not expect you’ll need it… all the time.