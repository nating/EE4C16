*These are instructions on how to set up the environment on mac for a [lab](https://github.com/frcs/EE4C16-self-driving-lab) by [François Pitié](https://francois.pitie.net/) for the module EE4C16 at [Trinity College Dublin](www.tcd.ie)*

# Lab 06 Mac Set-up

1. Download the repo zip by clicking [this](https://github.com/frcs/EE4C16-self-driving-lab/archive/master.zip).
2. Rename the folder from the zip file: "self-driving-lab".
3. [Download miniconda](https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh)
4. In your terminal, run `bash <the path to the .sh file that you just downloaded>` (Take note of the path that the terminal spits out for miniconda when you run this. Miniconda will add this to ~/.bashprofile, but this may not be where you need to have your exported paths. For instance, my terminal looks in ~/.zshrc when it starts up, so I had to put: `export PATH=<The path from when you downloaded miniconda>` in my .zshrc file.)
5. Quit Terminal and open it again for the changes to take effect.
6. Run `conda list` in your terminal to make sure that it is working.
7. Go to the "self-driving-lab" folder that you created earlier, and when inside, run the command `conda env create -f environment.yml`.
8. [Download the OSX version of the modified Udacity driving simulator](https://drive.google.com/open?id=1qqt_Q8pZqQFpvn9xHRMc002ABq-tQQDK)
9. Create a folder called "data" anywhere.

Now you should be all set to do [the lab](https://github.com/frcs/EE4C16-self-driving-lab) on your Mac!
