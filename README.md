## Docker

Starting nginx and all app containers

    docker-compose -f docker-compose.local.yaml up -d

(Re)building containers

    docker-compose -f docker-compose.local.yaml up -d --build

Once everything is build an running you can access the assembled product page via [http://localhost:3000/](http://localhost:3000/).

Individual apps are available at:

* <http://localhost:3001> (shell)
* <http://localhost:3002> (app1)
* <http://localhost:3002> (app2)

## Running Specific services

    docker-compose -f docker-compose.local.yaml up -d <servicename>
    docker-compose -f docker-compose.local.yaml down <servicename>

## References

* <https://chemidy.medium.com/create-a-small-and-secure-angular-docker-image-based-on-nginx-93452cb08aa2>
* <https://micro-frontends.org/>

## TODO

The subdirectory paths need to be managed in the angular routes or `<base>` during build to support both url forms.

Running the following against the application paths shows that the correct code is being returned:

    curl http://localhost:3000/shell/
    curl http://localhost:3000/app1/
    curl http://localhost:3000/app2/
