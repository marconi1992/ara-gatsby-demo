# Implementing Microfrontends in GatsbyJS using Ara Framework


## Setup

Install Dependencies for GatsbyJS project `gatsby-site`

```
$ yarn install
```

Install Dependencies for Nova service `novas/global`

```
$ yarn install
```

Install [Ara CLI](https://github.com/ara-framework/ara-cli)

```
$ npm install -g ara-cli
```

Install [Nova Static](https://github.com/ara-framework/nova-static)

```
$ export GOPATH=~/go

$ go get github.com/ara-framework/nova-static/nova-static

$ go install github.com/ara-framework/nova-static/nova-static

$ export PATH="$PATH:$GOPATH/bin"
```
## Running GatsbyJS

Run development server for GatsbyJS project:

```
$ yarn develop
```

Generate static website:

```
$ yarn build
```

Serve static files locally after generate static webiste:

```
$ yarn serve
```

## Running Nova service locally

Run Lambda locally:

```
$ ara run:lambda
```

Run Lambda locally with S3 server:

```
$ ara run:lambda --asset
```

## Running Nova Static

Define environment variables

```
$ export HYPERNOVA_BATCH=http://localhost:3000/batch

/* Relative path from the gatsby project */
$ export STATIC_FOLDER=./public
``` 

Execute `nova-static` command in `gatsby-site`

```
$ nova-static
```
