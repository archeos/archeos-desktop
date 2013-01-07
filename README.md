ARCHEOS DESKTOP METAPACKAGE
===========================

*This document is still in progress*

Simple instructions for this metapackage
----------------------------------------
1.   Edit the *debian/control* file and do the relative modifications (add package to depends, and so on)
2.   Update the changelog version with `dch -i`. Check that the distribution matches and describe what has been done
3.   Build the package with `debuild`. 
     If you don't want to sign it use `debuild -us -uc`.
     All files will be placed in the upper directory.
4.   Clean the package with `fakeroot debian/rules clean`.
5.   Upload the packages (all deb files, changes and dsc) to the repository server and import them into the distrubution with reprepro
