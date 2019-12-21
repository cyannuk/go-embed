## Go Embed
Generates go code to embed resource files into your library or executable.
This is more suitable for web servers as it gzip compresses all the files
automatically and computes the hash so that it can be used for caching the
assets in the frontends.

```bash
go-embed v2.0.0
Generates go code to embed resource files into your library or executable

  Usage:
    -input   string  The path to the folder containing the assets
    -output  string  The output filename
    -package string  The package name

  example:
    go-embed -input public/ -output assets/main.go
```

You can use this to embed your css, js and images into a single executable.

This is similar to [go-bindata](https://github.com/jteeuwen/go-bindata).

This is similar to [pony-embed](https://github.com/pyros2097/pony-embed).

This is similar to [rust-embed](https://github.com/pyros2097/rust-embed).

## Installation
```
go get github.com/cyannuk/go-embed
```

## Documentation
You can directly access your files as constants from the assets package or
you can use this func to serve all files stored in your assets folder which is useful for webservers and has gzip compression and hash creation for caching. Just see the example as to how same caching and compression works in
production and development.
```go
assets.Asset(path) (data, hash, contentType, error)
```

Go Gophers!

The power is yours!
