<img src="website/static/operator_logo_sdk_color.svg" height="125px"></img>

[![Build Status](https://travis-ci.com/operator-framework/operator-sdk.svg?branch=master)](https://travis-ci.com/operator-framework/operator-sdk)
[![License](http://img.shields.io/:license-apache-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)
[![Go Report Card](https://goreportcard.com/badge/github.com/operator-framework/operator-sdk)](https://goreportcard.com/report/github.com/operator-framework/operator-sdk)

## Documentation

Docs can be found on the [Operator SDK website][sdk-docs].

## Overview

This project is a component of the [Operator Framework][of-home], an
open source toolkit to manage Kubernetes native applications, called
Operators, in an effective, automated, and scalable way. Read more in
the [introduction blog post][of-blog].

[Operators][operator-link] make it easy to manage complex stateful
applications on top of Kubernetes. However writing an operator today can
be difficult because of challenges such as using low level APIs, writing
boilerplate, and a lack of modularity which leads to duplication.

The Operator SDK is a framework that uses the
[controller-runtime][controller-runtime] library to make writing
operators easier by providing:

- High level APIs and abstractions to write the operational logic more intuitively
- Tools for scaffolding and code generation to bootstrap a new project fast
- Extensions to cover common operator use cases

## Dependency and platform support

### Go version

Release binaries will be built with the Go compiler version specified in the Operator SDK's [prerequisites section][doc-readme-prereqs].

### Kubernetes versions

As the Operator SDK interacts directly with the Kubernetes API, certain API features are assumed to exist in the target cluster.
The currently supported Kubernetes version will always be listed in the SDK [prerequisites section][doc-readme-prereqs].

### Platforms

The following matrix defines which architectures are supported for GNU Linux:

|                               |     `amd64`     |     `arm64`     |    `ppc64le`    |     `s390x`     |
|-------------------------------|-----------------|-----------------|-----------------|-----------------|
| `operator-sdk`                | ✓               | ✓               | ✓               | ✓               |
| `ansible-operator`            | ✓               | ✓               | ✓               | ✓               |
| `helm-operator`               | ✓               | ✓               | ✓               | ✓               |
| `scorecard-test` image        | ✓               | ✓               | ✓               | ✓               |
| `scorecard-test-kuttl` image  | ✓               | ✓               | ✓               | -               |

The following matrix defines which architectures are supported for MacOS Darwin:

|                               |     `amd64`     |
|-------------------------------|-----------------|
| `operator-sdk`                | ✓               |
| `ansible-operator`            | ✓               |
| `helm-operator`               | ✓               |

Support for the Windows platform is not on the roadmap at this time.

## Community and how to get involved

- [Operator framework community][operator-framework-community]
- [Communication channels][operator-framework-communication]
- [Project meetings][operator-framework-meetings]

## How to contribute

Check out the [contributor documentation][contribution-docs].

## License

Operator SDK is under Apache 2.0 license. See the [LICENSE][license_file] file for details.

[controller-runtime]: https://github.com/kubernetes-sigs/controller-runtime
[license_file]:./LICENSE
[of-home]: https://github.com/operator-framework
[of-blog]: https://coreos.com/blog/introducing-operator-framework
[operator-link]: https://kubernetes.io/docs/concepts/extend-kubernetes/operator/
[sdk-docs]: https://sdk.operatorframework.io
[operator-framework-community]: https://github.com/operator-framework/community
[operator-framework-communication]: https://github.com/operator-framework/community#get-involved
[operator-framework-meetings]: https://github.com/operator-framework/community#meetings
[contribution-docs]: https://sdk.operatorframework.io/docs/contribution-guidelines/
