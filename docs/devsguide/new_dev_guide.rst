*********************
New Developer's Guide
*********************

==================
Setting up Github:
==================
Before you start using GitHub, you have to make Git available on your computer.
Even if it’s already installed, it’s probably a good idea to update to the
latest version. You can either install it as a package or via another installer
or download the source code and compile it yourself.

To download Git visit 
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git


-----------------
Installing on Mac
-----------------
On Mavericks (10.9) or above you can do this simply by trying to run git from
the Terminal the very first time. If you don’t have it installed already, it
will prompt you to install it. You might be prompted to install command line
developer tools if Xcode isn’t installed on your computer. 

If you want a more up to date version, you can also install it via a binary 
installer. An OSX Git installer is maintained and available for download at 
the http://git-scm.com/download/mac. This method will require Homebrew, which
may not already be on your device.


To Install Homebrew
```````````````````
Run the commands ::

	$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	$ brew doctor
	$ brew tap brewsci/science

---------------------
Installing on Windows
---------------------
There are also a few ways to install Git on Windows. The most official build is
available for download on the `Git website <http://git-scm.com/download/win>`__
and the download will start automatically. Note that this is a project called
Git for Windows (also called msysGit), which is separate from Git itself; for
more information on it, go to http://msysgit.github.io/.


-------------------
Installing on Linux
-------------------
If you want to install Git on Linux via a binary installer, you can generally do
so through the basic package-management tool that comes with your distribution.
If you’re on Fedora, for example, you can use yum: ::

$ sudo yum install git

If you’re on a Debian-based distribution like Ubuntu, try apt-get: ::

$ sudo apt-get install git

For more options, there are instructions for installing on several different
Unix flavors on the Git website, at http://git-scm.com/download/linux.

--------------------------------
Connecting Github account to Git
--------------------------------
For more detailed steps go `here 
<https://help.github.com/categories/bootcamp/>`__.

Overview:

1. In your computer's terminal, tell Git your name so your commits will be
properly labeled. ::
    $ git config --global user.name "YOUR NAME"
2. Tell Git the email address that will be associated with your Git commits. The
email you specify should be the same one found in your email settings on Github. ::
    $ git config --global user.email "YOUR EMAIL ADDRESS"
3. To contribute to the project, Fork PyNE’s `Github repository 
<https://github.com/pyne/pyne>`__.

Learn how to keep your email address hidden `here
<https://help.github.com/articles/keeping-your-email-address-private/>`__.

================
Installing PyNE:
================

There are a couple of methods outlined for downloading PyNE on this site
under `Installation <https://pyne.io/install/index.html>`__. For
developers, it is recommended that you install PyNE from the source.

Make sure that your device has all of the dependencies downloaded. You 
can check this by typing the name of the program into your command line 
followed by "-v" (e.g. $ python -v). If you are just starting as a 
developer, likely, you will not have all of the necessary components.

A particularly important detail to pay attention to is the version of
each dependency. For example, PyNE is currently supported in conda
install from 2.7.\* - 3.6.*, and attempting to install with a default
version of 3.7.\* will result in errors. Setting your version to be
compatible before you begin will help ensure you are successful.


-----------------------
Creating an Environment
-----------------------

If you already have Python installed through Anaconda, but it is not
compatible with the current version of PyNE, follow these steps to
create an environment for the conda install method.

#. Open a new shell in your terminal.
#. Run the command ::

	$ conda create -n py36 python=3.6 anaconda
        
	*  To run Python 2.7, or some other version, enter ::

			$ conda create -n py27 python=2.7 anaconda
	* "py27" serves as the name of the environment and "python=2.7"
			tells anaconda which version of Python to use in that 
			environment.
#. To enter the environment run ::

	$ conda activate py36

#. To leave enter ::
	
	$ conda deactivate

5. Before continuing with the PyNE `Conda Installation <http://pyne.io/install/
conda.html#conda>`__ ensure that the Python version is correct.



For additional support with creating and managing environments,
documentation can be found
`here
<https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-
environments.html#sharing-an-environment>`__.


==========================
Signing up for list hosts:
==========================
Everyone faces challenges sometimes when writing effective code. Thankfully, the PyNE developers can always be 
contacted on the list host at pyne-dev@groups.google.com. Another way to get 
help is by going to https://groups.google.com/forum/#!forum/pyne-users and 
joining the group to post. 

========================
Preparing to Contribute:
========================

From the documentation of git and GitHub, the skills of forking and
cloning are especially important to have mastered before beginning any
contribution to the repository.

Before forking this or any other repository, engage SSH keys. This will
make the process of cloning and making the repository a remote straight
forward. The process to enable SSH keys on your device is found in the
GitHub documentation
`here <https://help.github.com/en/github/authenticating-to-github/connecting-
to-github-with-ssh>`__.

To fork, clone, and then make the original repository a remote follow
these steps.

#. Go to `PyNE <https://github.com/pyne/pyne>`__.
#. Select Fork, and then your account.
#. In the command line, enter ::

	$ git clone git@github.com:USERNAME/pyne.git 
	Replace USERNAME with your account's name.
#. Then add the original repository as a remote to your account, first
   enter the clone on your device with the command "cd pyne".
#. Complete the process by entering ::
	
	$ git remote add upstream git@github.com:pyne/pyne.git


The PyNE files are now ready for your contributions. You can easily contribute 
by editing the contents of the folders, submitting these changes to your 
repository, and making a pull request to PyNE through Github’s website. 

=============
Contributing:
=============

Follow the `Developer's Guide <https://pyne.io/devsguide/index.html>`__
for contributions to this site, and PyNE itself.

----------------
Getting Practice
----------------
Novices to open-source projects can get still contribute to PyNE.  
To do so, go to PyNE’s `GitHub Page <https://github.com/pyne/pyne>`__ and, 
on the right-hand side of the page, select Issues. Once on this page, select 
the “low hanging pinoli” label to display more issues with the same tag.
Pinoli is the Italian word for the Pine Nut, and this marker is the 
first place New Developers should look to contribute.

---------------------------------
Adding and Updating Documentation 
---------------------------------
To contribute, you can edit the text file in any program that allows you to edit 
text (Vim, TextEdit, Nano, etc.) and doesn’t invisibly add characters to the 
file (like Word). The only important part is to write the file in a manner that’s 
considered reStructuredText (check out http://sphinx-doc.org/rest.html). Then, 
Sphinx will do everything else under the hood as described `here 
<http://pyne.io/devsguide/website.html>`__. Finally, commit these changes to 
your forked version and submit a pull request.
