# java-cli-millbuild-mysql-trigger

## Description
Creates a small database table
called `dog` with an `insert after` trigger.
The trigger function `ins_dog_trigger` calls `sp_rolling_audit`
that remmoves old entries. 


All output normally
seen in a terminal will be in `java-srv/log` which will dump to the screen. The project may seem to hang but the logs from the container must be written to the project this can take up to 3 min.

## Tech stack
- java
- millbuild
  - log4j
  - mysql driver

## Docker stack
- mariadb:latest
- nightscape/scala-mill

## To run
`sudo ./install.sh -u`
Creates java-srv/log

## To stop
`sudo ./install.sh -d`
Removes java-srv/log

## For help
`sudo ./install.sh -h`
