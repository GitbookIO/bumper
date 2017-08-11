
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

Bump X.0.0

```shell
$ gitbook-bumper -c -p minor
```

Bump 1.X.0

```shell
$ gitbook-bumper -c -p minor
```

Bump 1.0.X

```shell
$ gitbook-bumper -c -p patch
```

With a custom `package.json` directory

```shell
$ gitbook-bumper -d ./modules -c -p patch
```

Here is the preview of an interaction with the script:

```shell
$ gitbook-bumper -c -p minor

? Bump from 1.5.6 to 1.6.0 ? Yes
Writing version 1.6.0 to package.json...
Committing "Bump version to 1.6.0 :rocket:"...
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
    --no-confirm      do not ask for confirmation
    -c, --commit      make a commit and tag with version
    -p, --push        push commit and tag to remote

```
