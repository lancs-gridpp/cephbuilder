
Very basic scripts to fetch the ceph source code and build it in a docker container.

You will need tmux, buidah and docker/podman to use this script. The script doesn't do the final buidah commit of the container to create a new image.
The script only does the basics so there isn't a lot of error checking on inputs.  The progress panel doesn't show errors so you may need to check the log panel/file.

Usage: create <source image> <container name> [<ceph version>]

Example:
       create centos:stream9 cephpacificcs9 pacific
       create fedora:39 cephlatest

There are two scripts: create and do_create.  create configures tmux and then calls do_create to do the fetching and building.

