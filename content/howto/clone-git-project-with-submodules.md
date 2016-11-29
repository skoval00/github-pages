Title: Clone git project with submodules
Date: 2016-11-29 11:33

Some time ago I decided to store my local configuration files in git. But then I had to deal with the problem. What if I want to store some private employer-related settings in my config files? So I created two git repos: personal on the internet and private on my employers' premises.

I picked employers' repo as main project and added personal repo as submodule. Since I often forget how to initialize submodules after cloning, I wrote it down here.

After cloning the project one should issue next commands

    git submodule init
    git submodule update

Taken from [Git book](https://git-scm.com/book/en/v2/Git-Tools-Submodules#Cloning-a-Project-with-Submodules).
