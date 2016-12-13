---
title: xps 13 de
slug: xps-13-de
date: 12/12/2016
---

Guess what, gang? Your boy H. got a new computer! My old mid-2010 Macbook wasn't doing too great and gave me problems left and right. The final nail in the coffin was the battery died on me and required the computer to remain plugged in at all times. Not ideal by any means, and risky, since that can lead to the battery expanding and leaking. I was ready and willing to replace the battery myself and keep trudging along, but it turns out that Apple doesn't sell batteries to end consumers. I was left with the choice of paying Apple to replace it themselves, take a chance with a third party after market battery, or get a new Macbook. I love Apple, but decided it was time to move on.

I ended up getting the XPS 13 Developer's Edition laptop from Dell. Instead of the usual Windows, it comes pre-installed with Ubuntu. I'm no stranger to Linux, yet I've never used it as my daily driver. It's not without its quirks, but I'm impressed so far, and the hardware is beautiful. The only headache has been setting up my development environment and getting Linux to play nice with this site's CMS.

After installing php modules one by one and triple checking the directory and file permissions, I discovered I needed to enable mod_rewrite in Apache. Argh. But wait! I was still seeing 404 pages with every rewrite. It was then I realized I configured .htaccess wrong and I needed to point RewriteBase to the correct root directory. Finally! Kudos to the fine folks at Stack Overflow. I couldn't have done it without their help. 

The next challenge was integrating my git repository with my webhost. I've used git version control for the past year, and even though I'm decent with the most common commands, I still have difficulty with tasks above the beginner level. I haven't quite grasped how exactly one would migrate their dev files to a new computer and push to the origin server without running head first into a wall of merge conflicts. I've gone through this once before, and I had to resort to the same funky solution--I delete the old repo, then create a new, empty repo on github, and then push the site to the remote origin. This avoids having to resolve merge conflicts, but then I'm forced to re-deploy a ssh key and webhook to push my local commits to the live site. To further complicate matters, my webhost recently migrated the site to a new server and I didn't realize I was using my old public key and needed to generate new keys in order for the php webhook to function. Wonderful!  

It works now, or it seems to work, at least. It wouldn't surprise me if the site breaks in a randomly catastrophic way. I won't quit my day job.

**-H**
