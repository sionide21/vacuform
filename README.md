Vacuform
========

Vacuform is a thin wrapper around docker that lets you configure your dev for
the specific project you are working on.

It helps keep out the clutter that eventually builds when working on many
projects with different dependencies.

## Installation

Simply copy `bin/vacuform` to anywhere on your PATH

```
cp bin/vacuform /usr/local/bin
```

## Usage

To create an environment for a project:

```
vacuform init <base docker image>
```

You do not need to specify a base image. If omitted, the default of [ubuntu](https://hub.docker.com/_/ubuntu/) will be used.

To set up the environment:

```
vacuform conf
```

This will drop you into a shell in your docker image. Install any dependencies you need on the base image and then exit the shell. Your changes will be saved automatically.

Now you're ready to run your project:

```
vacuform exec <your normal commands>
```

For easier invocation, add the following to your bash profile:

```
alias ve="vacuform exec"
```

This will allow you to simply run `ve <your normal commands>`
