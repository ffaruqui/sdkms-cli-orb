# Description

An orb for using Fortanix SDKMS for your secrets, key management and cryptographic needs in your CircleCI jobs.

## Usage

See [this orb's listing in CircleCI's Orbs Registry](https://circleci.com/orbs/registry/orb/fortanix/sdkms-cli) for details on usage, or see below example:

## Example

In this example `config.yml` snippet, the required SDKMS parameter API endpoint is passed as parameter and API Key is stored as environment variable and then read as default parameter values by the `sdkms-cli` commands.

```yaml
version: 2.1
orbs:
  sdkms-cli: fortanix/sdkms-cli@x.y.z
workflows:
  your-workflow:
     jobs:
       - sdkms-cli/get-secret-value:
           api-endpoint: "https://sdkms.fortanix.com"
           api-key: "SDKMS_API_KEY"
           secret-name: "Some secret name"
           secret-file: ""
```

# Contributing

We gratefully accept bug reports and contributions from the community.
By participating in this community, you agree to abide by [Code of Conduct](./CODE_OF_CONDUCT.md).
All contributions are covered under the Developer's Certificate of Origin (DCO).

## Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
have the right to submit it under the open source license
indicated in the file; or

(b) The contribution is based upon previous work that, to the best
of my knowledge, is covered under an appropriate open source
license and I have the right under that license to submit that
work with modifications, whether created in whole or in part
by me, under the same open source license (unless I am
permitted to submit under a different license), as indicated
in the file; or

(c) The contribution was provided directly to me by some other
person who certified (a), (b) or (c) and I have not modified
it.

(d) I understand and agree that this project and the contribution
are public and that a record of the contribution (including all
personal information I submit with it, including my sign-off) is
maintained indefinitely and may be redistributed consistent with
this project or the open source license(s) involved.

# License

This project is primarily distributed under the terms of the Mozilla Public License (MPL) 2.0, see [LICENSE](./LICENSE) for details.
