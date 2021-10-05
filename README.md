# template_rust_rocket_api
Template for a rust api written with the rocket framework packaged in docker containers

Package.json only has the bash scripts for building, running and testing the project. Therefore npm is not required.

You can do the commands by just copy-pasting into a terminal in this folder.


You don't need rust installed to test this project either, but docker is.

Run commands with "npm run ${your_commands} in terminal. Here is what each of the package.json commands do:

## Docker commands

 - "docker-build": build an image of this project.
 - "docker-run": run previously built image as a docker container. You can test it with "requests.http" file in this root folder, need REST API vsCode extension.
 - "docker-stop": stop the container mentioned above. If container is not detached with -d, will need to call it in another terminal.
 - "docker-remove": stop container, remove container, then remove image of the container.
 - "docker-clear": delete every dangling images and containers.
 - "docker-clear-everything": delete every image and containers that aren't running.
 - "local-test": This is for those that doesn't want to install rustup. Compile and run unit tests for the project in a docker container.
 - "local-build": Compile in a docker container, then copy files to './target/release'.
 - "local-run": run compiled files from the command above.

## Commands without docker

If you don't have docker, but have rust in your computer.

 - Compile with "cargo build --target release"
 - Run with "cargo run --release"
 - Run unit tests with "cargo test"


