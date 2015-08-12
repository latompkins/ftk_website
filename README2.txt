Instructions

First, you should download Jekyll: http://jekyllrb.com/docs/installation/

Then, download this folder, and edit the necessary .md files.
If you want to add a new post, go to subdirectory _posts. Create a new .md file with the date on the file name, and write your post.
If you want to edit the sections (People/Publications/Introduction to Particle Physics/....), simply edit the corresponding .md files (1People.md, 2Publications.md, 3Introduction.md, ...)

Now you can update the website! Go to CMD, go to your lanyon folder, and enter the following commands:

jekyll build
scp -r _site/* your_stanford_id@corn.stanford.edu:/afs/ir/group/stanford_atlas/WWW/.

And the website is now updated!







