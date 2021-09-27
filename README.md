# Go package for tail-ing files

> The original https://github.com/hpcloud/tail does not seem to be maintained, I fork to maintain part of the code

This package is a fork of https://github.com/iiiusky which does not appear to be actively maintained.

A Go package striving to emulate the features of the BSD `tail` program.

```Go
t, err := tail.TailFile("/var/log/nginx.log", tail.Config{Follow: true})
for line := range t.Lines {
    fmt.Println(line.Text)
}
```

See [API documentation](http://godoc.org/github.com/iiiusky/tail).

## Log rotation

Tail comes with full support for truncation/move detection as it is
designed to work with log rotation tools.

## Installing

    go get github.com/iiiusky/tail
