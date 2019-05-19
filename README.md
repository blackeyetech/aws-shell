# Introduction

This image allows you to run **aws-shell** in a container.

See [here](https://github.com/awslabs/aws-shell) for more details on aws-shell.

You should bind mount your project directory to **/home/aws**.

NOTE: You need to ensure your **.aws** directory is in the root of your project
directory, unless you are going to run **configure**.

NOTE: The container is run as the user **aws**.

An example of using this container is as follows:

```
docker container run --rm -it \
                     --mount type=bind,src=$(pwd)/.aws,target=/home/aws \
                     blackeyetechnology/aws-shell
```

**aws-shell** is the default command.
