# Apt source.list database

Database of sources for distributions in the Debian family. Useful if you need
to get back to the "factory setting" of the apt sources used by the system.


## Creating a new entry in the database

When creating a new OS entry, create a directory with this name:

    sh -c '. /etc/os-release; echo $ID-$VERSION_ID'

Put the `sources.list` file in the directory, strip out all comments,
and don't include the `deb-src` entries. If there are files in `/etc/sources.list.d`
create that subdirectory and place the files in there.
