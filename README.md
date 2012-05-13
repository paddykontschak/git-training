Git-Training
============

There was a recent discussion over at one of Linus Torvalds' pull requests - rather, someone requested a pull on the Linux kernel through Githubs pull request option on the website - and Linus was making some very insightful objections about the current way the Github website creates pull requests.

You can read the whole discussion [here](https://github.com/torvalds/linux/pull/17#issuecomment-5654674). It's actually very interesting. Linus has been a developer for so many years that he developed a certain standard on how pull requests and commits should be formated. The guidelines have been on [git.kernel.org](http://git.kernel.org/?p=git/git.git;a=blob;f=Documentation/SubmittingPatches;h=ece3c77482b3ff006b973f1ed90b708e26556862;hb=HEAD) for years and they make a lot of sense.

---

So, what are these guidelines?

For Commits:

- make commits of logical units
- check for unnecessary whitespace with "git diff --check" before committing
- do not check in commented out code or unneeded files
- the first line of the commit message should be a short description (50 characters is the soft limit, see DISCUSSION in git-commit(1)), and should skip the full stop
- the body should provide a meaningful commit message, which:
	- uses the imperative, present tense: "change", not "changed" or "changes".
	- includes motivation for the change, and contrasts its implementation with previous behaviour
- add a "Signed-off-by: Your Name <you@example.com>" line to the commit message (or just use the option "-s" when committing) to confirm that you agree to the Developer's Certificate of Origin
- make sure that you have tests for the bug you are fixing
- make sure that the test suite passes after your commit

