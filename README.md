bashlive official repo
======================
official repo for BASHLIVE, a BASH communitysnippetfunctionframeworkcoderepository-tool for bashhackers

<img alt="" src="http://2webapp.com/bashlive/bashlive.png" style="height:0.8em"/>

see [HERE](https://github.com/coderofsalvation/bashlive) for the BASHLIVE-repo itself

### How to have your own repo 

The easiest way is look at 'index.txt', and create your own indexfile like so:

    /some/snippet/identifierpath    this is a description    http://raw.gist.github.com/ioiu3453$/raw

Bashlive can deal with the following formats:

    <path><tab><description><tab><url>
    <path><4 spaces><description><4 spaces><url>

Then store this indexfile on a webserver (or gist), and add the index-url to bashlive (described [here](http://bashlive.com/features.html#Privatecompletionrepos))

### Why generate an indexfile?

Because this index compiler will automatically find out the latest commits of (nonraw) gisturls.
This way, you don't need to update your indexfile when updating a gist (which is needed when you manually maintain a bashlive indexfile).

### How to add snippets to the official repo

Please fork it, add your files, and and do a pull request.
99% change I'll merge it.

more info on [bashlive see here](http://2webapp.com/bashlive)

### tips 
Browse the 'repo' tree, and you will see that every file contains two lines.
First line is the description, the second line is an url (usually raw gist-urls, github url e.g.)

    # some description
    https://gist.github.com/coderofsalvation/8338454/raw/substr.bash

### binary dependencies 
The contents of your gist-urls or text-urls with bashcode can contain this comment:

    # @dependency: sed grep

This will let bashlive check the dependencies, so it can inform the user about missing applications when being inserted.
Note: a number will mean that dependency functions from bashlive will also be fetched

### bashlive dependencies

If your item depends on bashlive items, just include them like so:

    # oneliner which does something 
    # @dependency: bashlive
    / :/bash/function/supercut!
    / :/bash/function/trim! 

    function foo(){
      curl "foo.com/bar.csv" | supercut 3 ',' | trim 
    }

NOTE: '!' forces sourcing without prompting the user
