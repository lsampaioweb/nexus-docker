# Nexus Docker Compose

You can access the project through the following link: https://libraries.homelab.

## Config Files:

We added a help file with the default configuration to connect Nexus and the OpenLDAP. Check the [ldap.txt](help/ldap.txt "ldap file") file.

Two other important help files are the [repositories.txt](help/repositories.txt "repositories file") and the [roles.txt](help/roles.txt "roles file").

## Folders:

1. Default folder.

``` bash
/opt/sonatype/nexus
```

2. Folder to add the certificates.

``` bash
/opt/sonatype/nexus/etc/ssl
```

## Commands:

1. Enter the container.

``` bash
docker exec -it nexus bash
```

## Backup:

  Execute Task "Backup".

## Restore:

  1. Stop Nexus Repository Manager.
  2. Remove the following directories from /nexus-data/db

``` bash
rm -r /nexus-data/db/{accesslog,analytics,audit,component,config,security}
```

  3. Go to the location where you stored the exported databases - "/nexus-backup" and copy the corresponding "*.bak" files to "/nexus-data/restore-from-backup" for restoration.

``` bash
cp /nexus-backup/*.bak /nexus-data/restore-from-backup/
```

  4. Restart Nexus Repository Manager.

## References:

1. [Docker Compose for Nexus Platform - Part 1.](https://blog.sonatype.com/docker-compose-for-nexus-platform "Docker Compose for Nexus Platform - Part 1")

1. [Docker Compose for Nexus Platform - Part 2.](https://blog.sonatype.com/docker-compose-for-nexus-platform-part2 "Docker Compose for Nexus Platform - Part 2")

1. [Nexus Repository Version Comparison.](https://www.sonatype.com/nexus-repository-oss-vs.-pro-features "Nexus Repository Version Comparison")

1. [Sonatype Nexus Repository Manager 3.](https://hub.docker.com/r/sonatype/nexus3 "Sonatype Nexus Repository Manager 3")

1. [Dockerized version of Nexus Repo Manager 3.](https://github.com/sonatype/docker-nexus3 "Dockerized version of Nexus Repo Manager 3")

1. [Configuring LDAP.](https://help.sonatype.com/repomanager3/nexus-repository-administration/user-authentication/ldap "Configuring LDAP")

1. [Gerar senha para uma aplicação enviar e-mail usando o servidor do Gmail.](https://myaccount.google.com/apppasswords "Gerar senha para uma aplicação enviar e-mail usando o servidor do Gmail")

1. [Automated Setup of Nexus Repository Manager.](https://blog.sonatype.com/automated-setup-of-a-repository-manager "Automated Setup of Nexus Repository Manager")

1. [Backup and Restore.](https://help.sonatype.com/repomanager3/backup-and-restore "Backup and Restore")

1. [Prepare a Backup.](https://help.sonatype.com/repomanager3/backup-and-restore/prepare-a-backup "Prepare a Backup")

1. [Configure and Run the Backup Task.](https://help.sonatype.com/repomanager3/backup-and-restore/configure-and-run-the-backup-task "Configure and Run the Backup Task")

1. [Restore Exported Databases.](https://help.sonatype.com/repomanager3/backup-and-restore/restore-exported-databases "Restore Exported Databases")

### License:

[MIT](LICENSE "MIT License")

### Created by:

1. Luciano Sampaio.
