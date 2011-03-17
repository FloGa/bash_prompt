bash_prompt
===========

Introduction
------------
This little gadget adds some (colorized) modifications to the BASH-prompt to
show extended information about an existing mercurial repository in the current
directory if there is one.

I got this idea from
<http://stevelosh.com/blog/2010/02/my-extravagant-zsh-prompt/>

Additionally I modified Steve's idea that had a great disadvantage: Everytime
the prompt refreshes it had to run serveral `hg`-commandos to display the
required information. On slower systems that could take some seconds for every
refresh. For example, my netbook took up to five seconds to refresh the prompt.
Hence, I added a feature to cache the information and just refresh it if it's
needed. The cache files are in `~/.prompt`, followed by the full path to the
repo. Every single piece of information is stored separately in its own plain
text file, so I could define refreshing conditions for every item separately if
I need to.

Requirements
------------
Obviously, mercurial must be installed and executable with the `hg`-command.
Additionally you need the `mq`-extension to be activated in your `~/.hgrc`.

Furthermore, you'll need `realpath` to be installed.
