# Php development boilerplate
A docker boilerplate for people who wants to develop a php application, useful for pure php applications or frameworks.

## Requirements
You will only need Docker installed on your machine (and docker-compose), please refer to this link for proper intallation: https://docs.docker.com/get-docker/.
Note that if ou are on Windows, you'll need also to have WSL installed.

## Installation 
1. Clone this project.
2. Launch the "docker-compose up --build" command.
3. Go to the root directory of your project and launch the command "chmod -R 777 ." (note that you may need to launch the command as sudo user if you are on unix-like systems).
4. If you are on Windows machines, you'll need to launch the command mentioned in point 3 using WSL, open from your search WSL, go to the root directory of the project, and launch te command "chmod -R 777 .".

## Using Vanilla PHP
This docker porject is already ready to use, you'll only need to be sure to have a file located in "src/public" called "index.php".

## Using frameworks
This project is ready for Laravel, Symfony or other frameworks. You'll need to use the composer service in order to launch the commands, good thing is you won't need to have composer intalled on your machine, since it is a service, if you need to switch to composer 1, just edit the version in the composer.dockerfile (FROM command) and use the version you prefer, then rebuild the environment with docker-compose.

As an example, I'll provide the intallation guide for Laravel here:
1. Launch the following command:  "docker-compose run --rm composer create-project laravel/laravel ." in the root of the project (be sure that /src folder is empty before launching).
2. Grant again all permissions in the root folder (chmod -R 777 .).
3.  You'll be able to access from http://localhost to your laravel homepage.

