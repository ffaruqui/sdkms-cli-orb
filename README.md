Easily install the Fortanix SDKMS SDKMS CLI in your CircleCI jobs.

## Usage

See [this orb's listing in CircleCI's Orbs Registry](https://circleci.com/orbs/registry/orb/ffaruqui_sandbox/sdkms-cli) for details on usage, or see below example:

## Example

In this example `config.yml` snippet, the required SDKMS parameter (API endpoint) and secret (API Key)  are stored, via [Contexts](https://circleci.com/docs/2.0/contexts), as environment variables in the `sdkms` context and then read as default parameter values by the `aws-cli/configure` command.

```yaml
version: 2.1

orbs:
  sdkms-cli: ffaruqui_sandbox/sdkms-cli@0.0.1

jobs:
  sdkms-cli:
    executor: sdkms-cli/default
    steps:
      - checkout
      - sdkms-cli/install

workflows:
  version: 2
  sdkms-cli:
    jobs:
      - sdkms-cli:
          context: sdkms
```
