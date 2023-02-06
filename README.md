# The starting place for all papers we write in RNL
This repo contains the official RNL paper template. _This should be your starting point each time you write a paper_,
whether for a conference or journal. Follow the instructions in this README. If you follow the
instructions, you’ll ensure that Dr. Humphreys can compile your LaTeX source without a hitch. If you don’t,
you’ll ensure he gets annoyed.


# Cloning, renaming, and creating new repo
In the steps below, replace ``new-paper`` with an identifier for the paper you're
writing.  For consistency with other paper repos, make it descriptive, lowercase,
and with hyphens separating words; e.g., cross-modal-plans-2020. 

    git clone --bare git@github.com:zackkomo/paper-template.git [new-repo-name]
    cd [new-repo-name]
    git push --mirror [new-repo-ssh]
    
# Compiling the paper
If your computer is set up with pdflatex, pangea has been cloned, and BIBINPUTS
and TEXINPUTS have been set as described above, you should be able to simply type
``make`` to compile the paper:

    make 

To clear out the automatically-generated intermediate files:

    make clean
    

Create a preprint version of the paper by adding a first-page footer like the one in [this paper](http://radionavlab.ae.utexas.edu/images/stories/files/papers/narula2018spsLimits.pdf) (for a conference) or [this paper](https://radionavlab.ae.utexas.edu/images/stories/files/papers/all_weather_50cm_journal.pdf) (for a journal).  Also add page numbering for pages 2 through the end.  You can do all this by uncommenting `%\preprinttrue` in the TeX file (so long as it was cloned from this `paper-template` repo), after filling in `\rfoot` and `\lfoot` appropriately.

