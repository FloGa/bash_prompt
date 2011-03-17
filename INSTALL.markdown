Install the bash_prompt
=======================

To activate your newly gotten, modified and colorized bash_prompt, just type

    . /path/to/bash_prompt

into your bash. That dot is not a typo, it's mandatory! It tells the bash to
execute the file, even the executable bit is not set. Of course you need to
replace /path/to/ with the actual path to bash_prompt.

To activate it from the beginning, so always you start a new bash, you can --
for example -- edit your ~/.bashrc. Open it with your favorite text editor and
add following lines:

    # enable the modified prompt for easier working with hg-repos
    if [ -f /path/to/bash_prompt ]; then
        . /path/to/bash_prompt
    fi

Also here, replace /path/to with the actual path. That `if`-`fi`-construction
tells the bash: First check if there really IS such a file. If true, execute
it. If you don't find it, just do nothing and go ahead. For the worst case
scenario that you move or even delete my bash_prompt, then your .bashrc won't
print error messages, even if you forget to remove those lines.
