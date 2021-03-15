_save
=====

A bookmarking utiliity. Can be used to easily save data inputs via the command 
line. Inputs can be categorized as an option.

Includes autocompletion functionnality for the categories.

Runs on ``bash``.

Installation
------------
*Tested On Ubuntu*

Download
********
Clone this repository in the directory of your choice

.. code-block::
    $ git clone https://github.com/gXiah/_save
    $ cd _save

Adding to PATH
**************
In order to be able to execute _save directly from the command line prompt, you 
can add the script file to your PATH.

First, rename the file to your convenience
.. code-block::
    $ mv _save <newName>
    
*from this point forwad, change "_save" to the <newName> you just chose*

Then, in order to add it to your PATH, you can do the following
**Note: This is in no way the only, nor the most optimal way to do it**

To temporarily add it to your PATH :
.. code-block::
    $ export  PATH=$(pwd):$PATH
    
To permanently add it for your personal use, copy the path or the directory
 in which ``_save``  is located.
.. code-block::
    $ echo "export PATH=$(pwd):$PATH" >> ~/.bashrc
    $ source ~/.bashrc
This will append the new PATH value to your ~/.bashrc file (and source it for an
imediate availability)


Adding the auto-complete feature
*******************************
Inside the cloned repository, you will find an ``auto_complete`` file. You can
install it using
.. code-block::
    $ source ./auto_complete


Modifiying the save path
************************

In order to modify the save path, open the _save file and modify the 
``$save_path_root`` variable



Usage
-----
*Tested On Ubuntu*

Basic usage
.. code-block::
    $ _save <category> <entry>

Will save the entry to a newly created category directory


No-category entries
.. code-block::
    $ _save <entry>

Will save the entry to a default category (see ``$DEFAULT_CATEGORY``).


Auto-completion
.. code-block::
    $ _save <tab><tab> 
will show the existing categories (if any)


Exceptions
----------

``$ _save `` alone will exit 2 and show the general syntaxe

