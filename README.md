This repo hosts the Go daemon that parses data received from the Rbkit
server gem. The incoming data is parsed and stored/processed for use by
the front-end built in Electron.

Installing pre-requisites
=========================

After you have a working Go installation on your machine, install the
ZMQ Go library by running:

```
go get github.com/vaughan0/go-zmq
```



Running the GC test
===================


In the Rbkit repo, run the `experiments/using_rbkit.rb` daemon. This
runs a sample script and has the rbkit server started.


Clone this repo, run `go run trigger_gc.go` to repeatedly
trigger the GC in the running ruby script.


To visualize if the GC is getting triggered or not, add a `puts
GC.stat(:count)` in the `using_rbkit.rb` file.
