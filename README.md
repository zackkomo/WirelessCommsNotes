# The starting place for all papers we write in RNL
This repo contains the official RNL paper template. _This should be your starting point each time you write a paper_,
whether for a conference or journal. Follow the instructions in this README. If you follow the
instructions, you’ll ensure that Dr. Humphreys can compile your LaTeX source without a hitch. If you don’t,
you’ll ensure he gets annoyed.


# Cloning, renaming, and creating new repo
In the steps below, replace ``new-paper`` with an identifier for the paper you're
writing.  For consistency with other paper repos, make it descriptive, lowercase,
and with hyphens separating words; e.g., cross-modal-plans-2020. 

    git clone git@gitlab.com:radionavlab/papers/paper-template.git new-paper
    cd new-paper
    git remote rename origin old-origin
    rm README.md
    git push --set-upstream git@gitlab.com:radionavlab/papers/new-paper.git master
    git remote add origin git@gitlab.com:radionavlab/papers/new-paper.git
    
Do not rename ``paper.tex``:  the directory name provides 
enough unique identification, and it's easier to compile and work with papers if 
they're all named ``paper.tex`` and ``paper.pdf``, etc.
    
# Setup

In some convenient location, clone the RNL writing resources repo:

    git clone git@gitlab.com:radionavlab/papers/pangea.git

To facilitate sharing of pangea with different directory structures, set the
environment variable BIBINPUTS on your platform to the full path to the pangea
directory.
  
Point LaTeX to our custom LaTeX style files by setting an environment
variable TEXINPUTS equal to the full path to pangea/texStyleFiles.
    
# Compiling the paper
If your computer is set up with pdflatex, pangea has been cloned, and BIBINPUTS
and TEXINPUTS have been set as described above, you should be able to simply type
``make`` to compile the paper:

    make 

To clear out the automatically-generated intermediate files:

    make clean
    

# Writing Your Paper

1. Read over the [Humphreys style
guide](https://gitlab.com/radionavlab/papers/pangea/blob/master/writing_resources/humphreys_guide.pdf).

2. Write your paper.

3. Go through the style guide section by section, point by point, and check 
  whether your paper is compliant on each point.

4. Spell check your paper.

5. Give your paper to Dr. Humphreys for review.

# Posting Your Paper

After you have submitted the final version of your paper to a conference for publication, or to a journal for review, do the following steps to ensure you paper gets 
maximum visibility:

1. Create a preprint version of the paper by adding a first-page footer like the one in [this paper](http://radionavlab.ae.utexas.edu/images/stories/files/papers/narula2018spsLimits.pdf) (for a conference) or [this paper](https://radionavlab.ae.utexas.edu/images/stories/files/papers/all_weather_50cm_journal.pdf) (for a journal).  Also add page numbering for pages 2 through the end.  You can do all this by uncommenting `%\preprinttrue` in the TeX file (so long as it was cloned from this `paper-template` repo), after filling in `\rfoot` and `\lfoot` appropriately.
2. Post the preprint version to the [RNL publications page](http://radionavlab.ae.utexas.edu/index.php?option=com_content&view=category&id=30&Itemid=37) by sending it to the current RNL website maintainer.
3. Optional: Post the preprint version to [arXiv] like [this example paper](https://arxiv.org/abs/2005.00709).
4. Create a BibTeX entry for your paper in [pangea.bib](https://gitlab.com/radionavlab/papers/pangea/-/blob/master/pangea.bib).  Be sure to follow the conventions you see there.  *Check first to ensure you're not creating a duplicate entry.*  The entry labeled `narula2020radarpositioning` is a good example for a conference publication.  The entry labeled `humphreys2019deepUrbanIts` is a good example for a journal publication.  For journal paper submissions, put `statusSub`, `statusRev`, or `statusTbp` in the `note` field (e.g., `note=statusSub`) as appropriate.  See the top of `pangea.bib` for definitions of these.  


# Responding to Peer Reviews

Reviewers dedicate valuable time to reading and critiquing our papers.  Their
points of criticism deserve consideration and a courteous response.  In
``responseToReviews/response_to_peer_reviews.tex`` you'll find a template review response.
_Note how a response was formulated for each point of criticism._  Nothing
bothers a reviewer more than to have a point ignored, or summarily dismissed,
without a proper rebuttal.

For most points, some concession can be made to the reviewer---a clarification,
an elaborated explanation, a caveat, an additional equation, a change of
notation, etc.  In a few rare cases, the reviewer has a misunderstanding that
is not prompted by a fair reading of the paper, or the reviewer is simply wrong
about a point of fact.  In these cases, proceed with polite firmness in
defending your position, and, if at all possible, add some extra term or
clarification to indicate responsiveness to the reviewer's point, even if
misguided.

After writing the response to reviews, write a brief cover letter addressed to
the associate editor handling the review process, and to the anonymous
reviewers, along the lines of ``responseToReviews/response_to_peer_reviews_cover_letter.tex``.
