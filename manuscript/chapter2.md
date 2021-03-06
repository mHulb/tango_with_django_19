#Getting Ready to Tango

Before we get down to coding it is really important that we get our development environment setup so that you can *Tango with Django!* You'll need to ensure that you have all the necessary components installed on your computer. This chapter outlines the five key components that you need to be aware or, setup and use:

* Working with the Command Line
* *Python* and your *Python* installation
* The Python Package Manager *pip* and *Virtual Environment* 
* Integrated Development Environment (IDE)
* Version Control System *Git* 


If you already have Python 2.7/3.5 and Django 1.9 installed and are familiar with the technologies mentioned, then you can skip straight to the [Django Basics chapter](#chapter-django-basics). Otherwise, below we provide an overview of the different components and why they are important. We also provide a series of pointers on how to setup the various components.


I> ###Development Environment 
I>
I> Setting up your development environment is pretty tedious and often a real pain because you only do it occasionally. 
I> Below we have put together the list of core technologies you need to get started and pointers on how to install them
I> It is a good idea when setting up your environment to note down the steps you took - because invariably you will forget 
I> the next time you go to re-install everything on a new machine or someone else's machine.


## Python
Tango with Django requires you to have installed on your computer a copy of the Python programming language. Any version from the `2.7` family (e.g. `2.7.5+`) or version `3.4+` will do. If you're not sure how to install Python and would like some assistance, have a look at **the chapter dealing with installing components**.

I> ### Not sure how to use Python?
I>
I> If you haven't used Python before or you simply wish to brush up on your skills, then we highly recommend that you check out and work through one or more of the following guides:
I> 
I> * [**Learn Python in 10 Minutes**](http://www.korokithakis.net/tutorials/python/) by Stavros;
I> * [**The Official Python Tutorial**](http://docs.python.org/2/tutorial/);
I> * [**Think Python: How to Think like a Computer Scientist**](http://www.greenteapress.com/thinkpython/) by Allen B. Downey; or
I> * [**Learn to Program**](https://www.coursera.org/course/programming1) by Jennifer Campbell and Paul Gries.


##Python Package Manager 
Pip is the python package manager, which lets you install various Python libraries. The package manager simplifies the process of upgrading and handling your packages. So you do not have to manually delete and remove libraries, or work out what dependencies the libraries you want to install have, as the package manager takes care of this. Also, you don't have to worry about added the libraries to the Python path, the package manager also takes care of this. If you don't have `pip` installed, go to the [System Setup Chapter](#chapter-system-setup), otherwise make sure you have the following installed:

{lang="text",linenos=off}
	pip install -U django==1.9.5
	pip install pillow

I> ### Problems Installing `pillow`?
I> When installing Pillow, you may receive an error stating that the installation failed due to a lack of JPEG support.
I> This error is shown as the following:
I> 
I> {lang="text",linenos=off}
I> 	ValueError: jpeg is required unless explicitly disabled using
I>              --disable-jpeg, aborting
I>
I> If you receive this error, try installing Pillow *without* JPEG support enabled, with the following command.
I>
I> {lang="text",linenos=off}
I> 	pip install pillow --global-option="build_ext"
I>                     --global-option="--disable-jpeg"
I>
I> While you obviously will have a lack of support for handling JPEG images, Pillow should then install without problem. For further information, check out the [Pillow documentation](http://pillow.readthedocs.io/en/3.2.x/installation.html).


##Virtual Environments

We're almost all set to go! However, before we continue, it's worth
pointing out that while this setup is fine to begin with, there are some
drawbacks. What if you had another Python application that requires a
different version to run? Or you wanted to switch to the new version of
Django, but still wanted to maintain your Django 1.9 project?

The solution to this is to use [virtual
environments](http://simononsoftware.com/virtualenv-tutorial/). Virtual
environments allow multiple installations of Python and their relevant
packages to exist in harmony. This is the generally accepted approach to
configuring a Python setup nowadays. 

Setting up a virtual environment is not necessarily but it is highly recommended. The [Virtual Environment Chapter](#chapter-virtual-environments) details how to setup, create and use virtual environments.


##Integrated Development Environment

While not absolutely necessary, a good Python-based integrated
development environment (IDE) can be very helpful to you during the
development process. Several exist, with perhaps JetBrains'
[*PyCharm*](http://www.jetbrains.com/pycharm/) and *PyDev* (a plugin of
the [Eclipse IDE](http://www.eclipse.org/downloads/)) standing out as
popular choices. The [Python
Wiki](http://wiki.python.org/moin/IntegratedDevelopmentEnvironments)
provides an up-to-date list of Python IDEs.

Research which one is right for you, and be aware that some may require
you to purchase a licence. Ideally, you'll want to select an IDE that
supports integration with Django.  

We use PyCharm as it supports virtual environments and Django integration - though you will have to configure the IDE accordingly. [PyCharm is also available for students](https://www.jetbrains.com/student/) - and JetBrains provides a graduate discount, too.

##Code Repository

We should also point out that when you develop code, you should always
house your code within a version-controlled repository such as
[SVN](http://subversion.tigris.org/) or [GIT](http://git-scm.com/). We
won't be going through this right now so that we can get stuck into
developing an application in Django. We have provided a
[crash course on GIT](#chapter-git). We highly recommend that you
set up a GIT repository for your own projects. Doing so will could save you
from disaster.

X> ###Exercises
X> 
X> To get comfortable with your environment, try out the following exercises.
X> 
X>  -   Install Python 2.7.5+/3.4+ and Pip.
X>  -   Play around with your CLI and create a directory called `code`,  which we use to create our projects in.
X>  -   Setup your Virtual Environment (optional)
X>  -   Install the Django and Pillow packages
X>  -   Setup an account on a Git Repository site like: GitHub, BitBucket, etc if you haven't already done so.
X>  -   Download and setup an Integrated Development Environment like [PyCharm](https://www.jetbrains.com/pycharm/)
X> 
X>  As previously stated, we've made the code for the book and application available on our [GitHub repository](https://github.com/leifos/tango_with_django_19/).
X> 
X>  -   If you spot any errors or problem, please let us know by making a change request on GitHub.
X>  -   If you have any problems with the exercises, you can check out the repository to see how we completed them.


