# ODB Dockerfile

The `odb` branch shows how to build `odb` using the same type of Docker commands
as used to build `vcf_validator`.

To build ODB using Docker for your local architecture:

```shell
REPO_NAME=my-odb make build-odb
```

To try it out:

```shell
docker run -it --rm my-odb/odb:2.5.0-b.23 odb --version
```

This alias is helpful to mount the current directory in Docker:

```shell
alias docker-run-here='docker run -it --rm --workdir "$PWD" --volume "$PWD:$PWD"'
```

```shell
docker-run-here my-odb/odb:2.5.0-b.23 odb --help
```
