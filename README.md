# Template Repository for Symfony Web Applications

## Initialise your repository
This a template repository. You can create another repository from this one by selecting the `use this template` button.

Your new repository will have the same structure as this one

## Initialise Symfony
Once you have created your Repository from this template use the command directly in your terminal :
```bash
$ ahoy init
```
**This command requires the [Symfony CLI](https://symfony.com/download). You need to have it installed !**

Do not forget to change the .dist files by deleting the .dist extension :
* ./.github/workflows/release.yaml.dist -> This is the CI for automated build of the app with Github Actions
* ./docker-compose.override.yaml.dist

Do not forget to check all TODOs :
* ./.github/worflows/release.yaml.dist
* ./docker-compose.yaml
* ./Dockerfile

## Initialise Docker
In this template, the `Dockerfile` is empty. You can use any Dockerfile you want. For every Namkin, you can use the base one available in any projects (take the latest one). With the default `Dockerfile`, you have to import the `docker` folder with the `nginx.conf` of the same project.

Then you have to uncomment the services you want in the `docker-compose.yaml`. Be careful, the `target: ` cannot be empty : if you use the default Dockerfile, you can set it to `dev` by default. The "TODOs" are here to help you.

Now, you can build your project locally
```
$ docker-compose up -d --build
```
