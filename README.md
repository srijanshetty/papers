papers
======

A git-annex repository of academic papers.

Using
-----

First install `git` and `git-annex`. Then:

```sh
git clone git://github.com/srijanshetty/papers
git-annex init local
git-annex get .
```

If you want just some particular paper:

```
git-annex get distributed-systems/2004-MapReduce.pdf
```

Please open an issue if you cannot download any paper so that I can mirror them.

How I created this?
-------------------

```sh
cd papers
git init
git remote add origin git@github.com/srijanshetty/papers
git-annex init laptop
git-annex addurl --file distributed-systems/PNUTS.pdf http://css.csail.mit.edu/6.824/2014/papers/cooper-pnuts.pdf
git-annex add .
git commit -m "papers"
git config remote.origin.annex-ignore true  # Because GitHub doesn't store annexed content. 
git push origin master git-annex
```

Who's Idea
----------

Blatantly copied the idea from @rejuveysh
