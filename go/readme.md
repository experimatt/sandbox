# Notes from my experience learning Go
The instructions to run the [Go Tour](https://tour.golang.org) locally are unclear. These are the steps I followed to get the Go Tour working locally.

Last updated: 11/3/2018

**Reference**
* [How to Write Go Code](https://golang.org/doc/code.html)
* [Test your installation](https://golang.org/doc/install#testing)

## Go Setup Instructions
This assumes you're on a mac, using fish, and have homebrew installed.

```
# install go
brew update
brew install go

# create ~/go directory
mkdir $HOME/go

# add this to config.fish
if test -d ~/go
  set -x GOPATH $HOME/go
  set -x PATH $PATH $GOPATH/bin
end

# restart terminal

# verify that go is installed 
go version
echo $GOPATH
echo $PATH
```

## Hello World (optional)
Note that the code snippets below no longer match the instructions linked below. Go no longer recommends making a go folder and setting a `GOPATH`, as far as I can tell (as of 12/2022).

----

To write your first Go program, follow the instructions at either of these links. **Your first program** seems to be more realistic and comprehensive.
1. [Your first program](https://golang.org/doc/code.html#Command)
2. [Test your installation](https://golang.org/doc/install#testing)

```
# create a base folder within your Go workspace
mkdir -p $GOPATH/src/github.com/user

# create a folder specifically for hello world
mkdir $GOPATH/src/github.com/user/hello
cd $GOPATH/src/github.com/user/hello

# create a `hello.go` file with the following contents
package main

import "fmt"

func main() {
	fmt.Println("Hello, world.")
}

# build and run the file
go install
hello
```

### [Go Tour](https://tour.golang.org)
Once you've got Go set up, you can install and run the go tour locally
```
# install go tour
go get golang.org/x/tour

# run it locally
tour
```
