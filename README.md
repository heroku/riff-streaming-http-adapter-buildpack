#
This is a fork of the now inactive https://github.com/projectriff/streaming-http-adapter-buildpack

# `gcr.io/projectriff/streaming-http-adapter`
The riff Streaming HTTP Adapter Buildpack is a Cloud Native Buildpack that provides the riff Streaming HTTP Adapter.

This buildpack is designed to work in collaboration with other buildpacks which request contributions of JREs and JDKs.

## Behavior
This buildpack will participate if all the following conditions are met

* Another buildpack requires `streaming-http-adapter`

The buildpack will do the following:

* Contributes a streaming HTTP adapter to a layer with all commands on `$PATH`

### Bindings
The buildpack optionally accepts the following bindings:

#### Type: `dependency-mapping`
|Key                   | Value   | Description
|----------------------|---------|------------
|`<dependency-digest>` | `<uri>` | If needed, the buildpack will fetch the dependency with digest `<dependency-digest>` from `<uri>`

## License
This buildpack is released under version 2.0 of the [Apache License][a].

[a]: http://www.apache.org/licenses/LICENSE-2.0
