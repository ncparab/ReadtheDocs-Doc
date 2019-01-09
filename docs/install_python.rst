############################
 Install Python 2.7
############################

- In order to compile Python you must first install the development tools and a few extra libs. The extra libs are not strictly needed to compile Python but without them your new Python interpreter will be quite useless.
Execute all the commands below as root either by temporarily logging in as root or by using sudo.

.. code-block:: bash

        $yum update

        $yum groupinstall -y "development tools"

        $yum install -y zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel expat-devel

        $yum install -y wget

Download, Compile and Install Python
-------------------------------------

.. code-block:: bash

        # Python 2.7.14:

        $wget http://python.org/ftp/python/2.7.14/Python-2.7.14.tar.xz
    
        $tar xf Python-2.7.14.tar.xz

        $cd Python-2.7.14

        $./configure --prefix=/usr/local --enable-unicode=ucs4 --enable-shared LDFLAGS="-Wl,-rpath /usr/local/lib"

        $make && make altinstall


Install/Upgrade pip,Setuptools and wheel
-----------------------------------------

Each Python interpreter on your system needs its own install of pip, setuptools and wheel. The easiest way to install or upgrade these packages is by using the get-pip.py script.

.. code-block:: bash

        # First get the script:

        $wget https://bootstrap.pypa.io/get-pip.py

        # Then execute it using Python 2.7 and/or Python 3.6:

        $python2.7 get-pip.py

        
- With pip installed you can now do things like this:

.. code-block:: bash

        $pip2.7 install [packagename]

        $pip2.7 install --upgrade [packagename]

        $pip2.7 uninstall [packagename]

        $pip2.7 install virtualenv

- Check the system Python interpreter version:

.. code-block:: bash

        $python --version
