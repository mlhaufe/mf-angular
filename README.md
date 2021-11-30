## Docker

Starting nginx and all team containers

    docker-compose -f docker-compose.local.yaml up -d

(Re)building containers

    docker-compose -f docker-compose.local.yaml up -d --build

Once everything is build an running you can access the assembled product page via [http://localhost:3000/](http://localhost:3000/).

## Running Specific services

    docker-compose -f docker-compose.local.yaml up -d <servicename>
    docker-compose -f docker-compose.local.yaml down <servicename>

## References

- https://chemidy.medium.com/create-a-small-and-secure-angular-docker-image-based-on-nginx-93452cb08aa2
