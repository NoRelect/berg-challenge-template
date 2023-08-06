# berg-challenge-template

This is a template repository for creating a challenge that can be deployed using the berg ctf platform.

## Structure

### challenge-handout

This folder contains all files that you want to give to the players of the ctf.
Files in this folders do not need to be compressed, an archive of all files in this directory
will be created automatically.

Most of the time, files in this folder are identical to the files in `challenge-src`, but with
the correct flag replaced with a placeholder value.

### challenge-solution

This folder contains a writeup and an optional solution script that can be used to solve the challenge.

### challenge-src

This folder contains the files that are used to actually run the challenge. There must be one or
more `Dockerfile`'s that can be used to build the challenge containers.

### challenge.yaml

This file is a kubernetes custom resource definition file of a `Challenge` as it is required
in the berg platform. It contains all the metadata needed for a challenge, such as expected
difficulty level, applicable categories, the correct flag and how to run the containers and
what ports to expose.
