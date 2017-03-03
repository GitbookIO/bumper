
# gitbook-bumper

Bump your Node modules using GitBook's convention for SemVer!

## Installation

This module just contains one script `bin/gitbook-bumper`.


### Global

You can install this script globally using:

```shell
npm install -g gitbook-bumper
```

### Local

You can also install it locally to your project:

```shell
npm install --save-dev gitbook-bumper
```

It will be accessible from the command line if you added `node_modules` to your path.

## Example

```shell
$ gitbook-bumper --commit --pushing --push major

? Bump from 0.0.1 to 1.0.0 ? Yes
Writing version 1.0.0 to package.json...
Committing "Bump version to 1.0.0 :rocket:"...
Tagging...
Pushing...
Pushing tags...
Done.
```

## Usage

```
  Usage: gitbook-bumper [options] <level> [prerelease-id]

	 Where level is one of major, minor, patch, premajor, preminor, prepatch, prerelease

  Options:

    -h, --help        output usage information
    -V, --version     output the version number
    -d, --dir <path>  directory of the Node module (default './')
    -f, --force       do not ask for confirmation
    -c, --commit      make a commit and tag with version
    -p, --push        push commit and tag to remote

```

