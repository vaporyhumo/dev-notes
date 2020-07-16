# Docker
#### Docker w/ Rails
Ejemplo oficial de como usar rails con docker y `docker-compose`.
* [https://docs.docker.com/compose/rails/](https://docs.docker.com/compose/rails/)

#### Alia
Algunos aliases útiles para trabajar con docker:
```sh
# to claim back ownership of docker created files
alias own='sudo chown -R $USER:$USER .'
```

#### Permission Issues
Algo de documentación para los problemas que hay con la autoría de archivos creados desde un contenedor.
* [https://vsupalov.com/docker-shared-permissions/](https://vsupalov.com/docker-shared-permissions/)
* [https://medium.com/@nielssj/docker-volumes-and-file-system-permissions-772c1aee23ca](https://medium.com/@nielssj/docker-volumes-and-file-system-permissions-772c1aee23ca)
* [https://help.ubuntu.com/community/FilePermissions](https://help.ubuntu.com/community/FilePermissions)
