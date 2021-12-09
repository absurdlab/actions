# Actions

Reusable Github Actions.

## `go_test`

Executes Go tests with optional tag support.

**input**

_Bold are required_

| Name       | Description                    | Default |
|------------|--------------------------------|---------|
| go_version | Version of Go                  | `^1.16` |
| tags       | Build tags                     |         |
| base_dir   | Directory of tests in the repo | `.`     |

## `image`

Build docker image and optional push to repository.

_Bold are required_

**input**

| Name       | Description               | Default       |
|------------|---------------------------|---------------|
| context    | Docker build context      | `.`           |
| **images** | List of image names       |               |
| tags       | Image tagging strategy    | see yaml      |
| build_args | Docker build args         |               |
| platforms  | List of target arch       | `linux/amd64` |
| push       | Whether to push to remote | `false`       |
| registry   | Remote registry address   | `ghcr.io`     |

**secret**

| Name              | Description           |
|-------------------|-----------------------|
| registry_username | Username for registry |
| registry_password | Password for registry |



