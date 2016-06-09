User Installation
=================

1. Configure your git credentials:

        git config --global user.name "Your Name"
        git config --global user.email "you@example.com"

2. Install requirements:

        sudo apt-get install wget git python python-virtualenv python-dev python3-dev python3-pip

3. Download git-repo:

        wget https://storage.googleapis.com/git-repo-downloads/repo
        chmod a+x ./repo

4. Get manifest files:

        ./repo init -u https://gitlab.tkn.tu-berlin.de/wishful/wishful_manifests.git

5. Configure user-only manifest file:

        ./repo init -m user.xml

6. Get all repositories:

        # to get all repositories
        ./repo sync
        # to create master branch on all
        ./repo start master --all
        # to check status of all repositories
        ./repo status


Developer Installation
======================

1. Create an account at our gitlab -> Go to: https://gitlab.tkn.tu-berlin.de/

2. Upload your public key into you account settings.

3. Install requirements:

        sudo apt-get install wget git python python-virtualenv python-dev python3-dev python3-pip

4. Download git-repo:

        wget https://storage.googleapis.com/git-repo-downloads/repo
        chmod a+x ./repo

5. Now that we have repo, you can clone all your projects in one easy command:

        ./repo init -u ssh://git@gitlab.tkn.tu-berlin.de/wishful/wishful_manifests.git

6. Then from there just run:

        # to get all repositories
        ./repo sync
        # to create master branch on all
        ./repo start master --all
        # to check status of all repositories
        ./repo status


Installation
============

1. Create virtual environment:

        virtualenv -p /usr/bin/python3 ./dev

2. Activate virtual environment:

        source ./dev/bin/activate

3. Install all dependencies (if all needed):

        pip3 install -U -r ./.repo/manifests/requirements.txt

4. Deactivate virtual environment (if you need to exit):

        deactivate

Running examples
================

1. Example controller:

        #to enable debug mode run with parameter -v
        cd ./examples/simple
        ./wishful_simple_controller --config ./controller_config.yaml

2. Example agent

        #to enable debug mode run with parameter -v
        cd ./examples/simple
        ./wishful_simple_agent --config ./agent_config.yaml