## Introduction

Here, you have to write 4 sentences maximum to provide a clear description of the project.
What are the goals, who should use it.

## Requirements

* php >= <version>
* Symfony >= <version>
* Docker & docker-compose
* [Node.js](https://nodejs.org/en/)
* [npm](https://nodejs.org/en/)
* [GitHub Packages Token](https://wiki.namkin.fr/dev/dev-env/general)

## Installation

### docker-compose.yaml
To install this project, clone this project on your device. Rename the `docker-compose.override.yml.dist` file to `docker-compose.override.yml`.
In the override file, you are able to change the port you want to use to run this project.

### Install container
You can now install the containers thanks to **docker-compose**. The first time, it will install your environment on your containers.

    docker-compose up -d

### Install php bundles
You can now access your containers with `docker-compose exec <container_name> bash` or use `ahoy tty` to access your _app_ container. Once you are in this container, you have to install Symfony and all its dependencies (that are listed in the `package.json` file). To do this you only have to do :

    composer install

### Environment variables
You need to set up the environment variables in the `.env` file (you can create a `.env.local` to override the `.env` configuration only on your device) :

`.env` variable | Default Value | Details
--------------- | ------------- | -------
`DATABASE_URL` | `mysql://root:test@db:3306/<project_name>-site` | This is the url of your database.
`ANOTHER_ENV_VAR` | `<default_value>` | Provide a short description of this variable

### Commands

| Command | Description | Comments |
| --- | --- | --- |
| `npm run serve` | Compiles and hot-reloads for development | - |
| `npm run build` | Compiles and minifies for production | - |
| `npm run dev` | Compiles and minifies back-end assets | - |
| `npm run dev` | Compiles and hot-reloads back-end assets | - |

Once you have everything set up, you are able to access your projet locally, on the port you have set up in `docker-compose.yaml`

## Deployment

With Docker, we can build images and push as we want. We have implemented a Continuous Integration (aka. CI) to make this task faster and easier: on each successful release on the Github Repository, the CI will build an image and push it on our Registry.

To deploy the newest version of the project on your server, you only have to make a `docker-compose.yaml` file and set up the app container with the version of your choice of the image on the registry. You can always have the latest version of the project thanks to the tag `:latest`.

Then you have to pull the chosen image from the registry :

    docker pull gcr.io/namkin/<project-name>:<tag>

And you can run

    docker-compose up -d

## Configuration

Optional informations about the customization you can have to configure the project with examples.

## Further Documentation

You can check the documentation of the bundle we use:
* [Symfony](https://symfony.com/doc/current/index.html)