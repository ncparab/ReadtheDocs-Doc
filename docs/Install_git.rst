###################################
 Install Latest git
##################################
 
 Before installing Git from source code, make sure you have already installed required packages on your system. If not use the following command to install the required packages.

- Use below command

.. code-block:: bash
       
         $yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel

         $yum install gcc perl-ExtUtils-MakeMaker

- Install Git on CentOS & Fedora

.. code-block:: bash
  
         $wget https://www.kernel.org/pub/software/scm/git/git-2.20.1.tar.gz

         $tar xzf git-2.20.1.tar.gz

- After downloading and extracting Git source code, Use the following command to compile the source code.

.. code-block:: bash
       
        $cd git-2.20.1

        $make prefix=/usr/local/git all

        $make prefix=/usr/local/git install

- Setup Environment

After installation of git client. Now you just need to set binary in the system environment. Set the PATH variable with newly installed git binary in /etc/bashrc by executing below command. Also, reload the changes in the current environment.

.. code-block:: bash
         
        $echo "export PATH=/usr/local/git/bin:$PATH" >> /etc/bashrc

        $source /etc/bashrc

- After completing the steps. Let’s use the following command to check the current git version.

.. code-block:: bash
         
        $git --version

-Output >> git version 2.20.1
