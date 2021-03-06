.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


Setting up a workstation requires the following:

#. Install a development environment:

   * Debian based (apt): ``apt-get install build-essential``
   * RHEL based (yum): ``yum groupinstall "Development Tools"``
   * OS X: ``xcode-select --install``

#. Install |git|: http://git-scm.com/book/en/v2/Getting-Started-Installing-Git.
#. Install the |chef dk|: https://downloads.chef.io/chef-dk/. Be sure to follow all instructions; for example, to run delivery commands you must set the following:  
   
   ``echo 'eval "$(chef shell-init bash)"' >> ~/.bash_profile``

#. Install ``knife push``: ``chef gem install knife-push``.
