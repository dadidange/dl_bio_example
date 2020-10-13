# dl_bio_example

Download the dataset on:
https://www.kaggle.com/prasunroy/natural-images
Unzip and remove the data folder (for some reason the data are save two times).

## Files:

### docker/docker_build.sh

Script to build a Docker-Image based on a Dockerfile in the same folder. See Section
"Docker" for further information.

### docker/Dockerfile

A file containing all the dependencies and information on the folder structure, etc. of 
the project. This file must be named "Dockerfile"!

### config.py

Contains parameters for launching the run_training.py

### docker_run.sh

Sript to launch a Docker-Container based on the image that is generated by the
docker_build.sh script. See Section "Docker" for further information.

### run_training.py

The starting point of the project. Execute this file to launch the training process.

### train_interfaces.py

A supplementary file for the training process.

## Docker

Upon execution of the docker_build.sh script, a Docker-Image will be created. This image
will be based on the Dockerfile. Henceforth, you will always have to rebuild the image
when your dependencies change or are updated (like for example the DLBio-repository).
Execute the docker_run.sh script to launch a Docker-Container in your terminal. This
container will be based on the Docker-image that was created by the docker_build.sh.
You can run Files the same way as you would in any other terminal.

More on docker with vs-code:
https://moodle.uni-luebeck.de/mod/forum/discuss.php?d=33479

## Debugging:

The Debugger has two options. Select "Docker: Python - General" to start debugging the
project from its main file. Select "Docker: Python - Current" to start debugging the
currently in the editor selected file.
More configurations can be added or present configurations can be changed in the
./vscode/launch.json and ./vscode/tasks.json.
