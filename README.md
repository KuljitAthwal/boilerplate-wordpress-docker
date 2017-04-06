# boilerplate-wordpress-docker
Docker environment for Wordpress development

## About

This is a small project, which replicates many others, to help me get to grips with Docker. I use this to help me set up a dev environment for Wordpress theme and plugin development. A process which I hope to automate using this project.

## Install

Use docker-compose to build the image and run the two services; wordpressdb, wordpress
Run the following command in PowerShell or cmd or a CLI of your choosing.
```
docker-composer up
```

## Usage
Run the following command in PowerShell or cmd or a CLI of your choosing to display the created images
```
docker images
```

Run the following command in PowerShell or cmd or a CLI of your choosing to display the running instances
```
docker ps
```

wordpressdb is the mysql container. This container is used by the wordpress container to store the database for the Wordpress install. A volume, db_data, has also been configured to persist the database

The Wordpress application files are cloned as part of the build process from the github repository : https://github.com/WordPress/WordPress

The themes and plugins folders are set up as volumes so that custom theme and plugin development can be carried out on the host machine. However there is an issue in that the default contents of the themes and plugin folders are overwritten as soon as the volumes are configured. I am currently working on a better solution for this.

Navigate to http://localhost:8000 in your browser to begin the Wordpress installation. By default the database credentials you need to use are as follows

- db name : wordpress
- db username : wordpress
- db password : wordpress
- db host : wordpressdb

## Coming Soon
- The addition of a default boilerplate theme using Bootstrap
- Configuration management to allow for custom database names, credentials, port mapping etc.

## License

MIT © [Kuljit Athwal](http://kuljit.com)