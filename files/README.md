README

# Build

    $ docker build -t docker-registry .


# Run

    $ docker run -d -p 5000:5000 -e SETTINGS_FLAVOR=private docker-registry


# Register itself

    $ docker tag docker-registry localhost:5000/docker-registry
    $ docker images
    REPOSITORY                       TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
    localhost:5000/docker-registry   latest              6d44c2e2a7ff        3 minutes ago       2.841 GB
    docker-registry                  latest              6d44c2e2a7ff        3 minutes ago       2.841 GB
    ...

    $ docker push localhost:5000/docker-registry
    The push refers to a repository [localhost:5000/docker-registry] (len: 1)
    Sending image list
    Pushing repository localhost:5000/docker-registry (1 tags)
    511136ea3c5a: Pushing [=======>                                           ] 1.536 kB/10.24 kB 2s
    46e4dee27895: Pushing [=====>                                             ] 1.024 kB/10.24 kB 2s
    0e5997dad26c: Pushing [=================================================> ] 144.5 MB/144.7 MB 0
    f33cb1127994: Pushing [=================================================> ] 32.72 MB/32.79 MB 0
    b865a7ff0001: Pushing [=================================================> ] 240.2 MB/240.3 MB 0
    4e464daabd63: Pushing [=================================================> ] 1.018 MB/1.024 MB 0
    7ceee811afc9: Pushing [=================================================> ] 63.18 MB/63.23 MB 0
    ddabfd862ae5: Pushing [=========================>                         ]  5.12 kB/10.24 kB 1s
    3ada39823d03: Pushing [=====>                                             ] 1.024 kB/10.24 kB 4s
    2e8620a1f0a7: Pushing [=====>                                             ] 1.024 kB/10.24 kB 2s
    6d44c2e2a7ff: Pushing [============>                                      ]  2.56 kB/10.24 kB 0
    Pushing tags for rev [6d44c2e2a7ff] on {http://localhost:5000/v1/repositories/docker-registry/tags/latest}


