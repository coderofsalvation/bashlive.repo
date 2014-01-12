bashlive official repo
======================
official repo for BASHLIVE, a BASH communitysnippetfunctionframeworkcoderepository-tool for bashhackers

<img alt="" src="http://2webapp.com/bashlive/bashlive.png" style="height:0.8em"/>

### How to add snippets to the official repo

Please fork it, add your files, and and do a pull request.
99% change I'll merge it.

more info on [bashlive see here](http://2webapp.com/bashlive)

### tips 
Browse the 'repo' tree, and you will see that every file contains two lines.
First line is the description, the second line is an url (usually raw gist-urls, github url e.g.)

    # some description
    https://gist.github.com/coderofsalvation/8338454/raw/substr.bash

### dependancies 
The contents of your gist-urls or text-urls with bashcode can contain this comment:

    # @dependancy: sed grep 123

This will let bashlive check the dependancies, so it can inform the user about missing applications when being inserted.
Note: a number will mean that dependancy functions from bashlive will also be fetched

