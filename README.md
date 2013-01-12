ARCHEOS DESKTOP METAPACKAGE
===========================

*This document is still in progress*

Requirements
------------
1.   git-buildpackage

Simple instructions for this metapackage
----------------------------------------
1.   Edit the *debian/control* file and do the relative modifications (add package to depends, and so on).
2.   You can test the package build with `git-buildpackage --git-ignore-new` anytime you want.
3.   When ready to deploy a working version, commit your changes the usual way (`git add` & `git commit`).
4.   Use `git-dch -R` to update the changelog file. 
     Edit it properly (if need to change something, but most of the time it doesn't.) then add it and 
     commit it too (usual`git add` and `git commit`).
5.   Build and tag the package with `git-buildpackage --git-tag`. Push changes upstream 
     with `git push && git push --tags`
6.   Clean the package with `debuild clean`.
7.   Upload the packages (all deb files, changes and dsc) to the repository server and import them into 
     the distrubution with reprepro.
