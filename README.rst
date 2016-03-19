#######################################
Face++ Cli
#######################################

This is an interactive Face++ command line tool which is used to call the Face++ API.

--------------------------
Features
--------------------------

Here is providing two methods to call Face++ API, one is interfactive command line,
another is python scripting. Both methods are used the shared api file ``facepp.py``
which is the Face++ API implemented with Python.

For the features, 3 main folders provided:

- ``faceapi``: ``facepp.py`` is the Face++ API. 
- ``cli``: the command line tool of calling Face++ API.
- ``demo``: a demo code for calling the Face++ API with python script.

Folder Structure

::

    ./facepp-cli
        \
        \-------- faceapi/               # Face++ API
        \-------- cli/                   # the command line tool
        \-------- demo/                  # a demo code with Python SDK
        \-------- images/                # image samples
        \
        \-------- licenses/

--------------------------
Getting Started
--------------------------

How to call Face++ API:

::

    Singup Face++ --> Create an App --> Generate KEY and SECRET --> API Call (Cli/Scripting)

Step 1. Signup
~~~~~~~~~~~~~~~~~~

Enter `Face++`_ official site, and signup a new account.

.. _`Face++`: http://www.faceplusplus.com

Step 2. App
~~~~~~~~~~~~~~~~~~

Go to the dashboard, create a new app, and then find out the ``API_KEY`` and ``API_SECRET``.
For the details, please reference the official instruction: `Getting Started`_.

.. _`Getting Started`: http://www.faceplusplus.com/create-a-new-app/


Step 3. API Call
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

3 main methods are available:

- ``cli``: command line
- ``demo``: python script
- ``faceapi``: customization to your personal app

---------------------------
API Call: cli
---------------------------

Try the command line:

- ``cli``: ``cd`` to this folder
- ``apikey.cfg``: add the ``API_KEY`` and ``API_SECRET`` into this file
- ``cli.py``: type ``python cli.py`` to start the interactive command line

::

    # clone the project
    $ cd /to/project_path
    $ git clone https://github.com/arttechresearch/facepp-cli

    # cd to facepp-cli/cli
    $ cd facepp-cli
    $ cd cli
    
    # add API_KEY and API_SECRET to apikey.cfg
    $ cp apikey.sample.cfg apikey.cfg
    $ vim apikey.cfg                     # add API_KEY and API_SECRET

    # run cli.py
    $ python cli.py


Command Line:

::

    api.detection.detect(img = File(r'<path to the image file>'))

----------------------------
API Call: scripting
----------------------------

Try the scripting:

- ``demo``: ``cd`` to this folder
- ``hello.py``: add the ``API_KEY`` and ``API_SECRET`` into this file
- ``hello.py``: run the script with ``python hello.py``

::

    # clone the project
    $ cd /to/project_path
    $ git clone https://github.com/arttechresearch/facepp-cli

    # cd to facepp-cli/demo
    $ cd facepp-cli
    $ cd demo

    # add API_KEY and API_SECRET to hello.py
    $ vim hello.py                     # add API_KEY and API_SECRET
    
    # run hello.py
    $ python hello.py

----------------------------------
API Call: writing your app
----------------------------------

customize to anywhere:

- ``api``: copy this folder to your personal project
- initialize an api


::

    # clone the project
    $ cd /to/project_path
    $ git clone https://github.com/arttechresearch/facepp-cli
    
    # cd to facepp-cli
    $ cd faceapp-cli
    
    # copy faceapi to your project
    $ cp faceapi /path/to/project

Python Call

::

    from faceapi.facepp import API
    api = API(API_KEY, API_SECRET)

-------------------------
Face++ API
-------------------------

- `Face++ API docs`_

.. _`Face++ API docs`: http://www.faceplusplus.com/api-overview/
