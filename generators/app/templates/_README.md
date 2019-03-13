# <%= name %>

> This project was generated by [generator-tf-module](https://github.com/sudokar/generator-tf-module)

## Overview

<%= description %>

## Usage

```hcl
module "<%= name %>" {
  source = "git::ssh://"
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| mandatory | this field is mandatory | string | n/a | yes |
| optional | this field is optional | string | `"default_value"` | no |

## Outputs

| Name | Description |
|------|-------------|
| output\_name | description for output_name |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Development

### Prerequisites

- [terraform](https://learn.hashicorp.com/terraform/getting-started/install#installing-terraform)
- [terraform-docs](https://github.com/segmentio/terraform-docs)
- [pre-commit](https://pre-commit.com/#install)
<% if (testFramework == '1') { %>
- [golang](https://golang.org/doc/install#install)
- [golint](https://github.com/golang/lint#installation)
<% } %>
<% if (testFramework == '2') { %>
- [ruby](https://rvm.io/)
<% } %>

### Configurations

- Configure pre-commit hooks
```sh
pre-commit install
```

<% if (testFramework == '1') { %>
- Configure golang deps for tests
```sh
> go get github.com/gruntwork-io/terratest/modules/terraform
> go get github.com/stretchr/testify/assert
```
<% } %>
<% if (testFramework == '2') { %>
- In the module root directory, install ruby gems for tests
```sh
bundle install
```
<% } %>

### Tests

- Tests are available in `test` directory
<% if (testFramework == '1') { %>
- In the test directory, run the below command
```sh
go test
```
<% } %>
<% if (testFramework == '2') { %>
- In the module root directory, run the below command
```sh
bundle exec kitchen test
```
<% } %>

## Authors

This project is authored by below people

- <%= author %>

> This project was generated by [generator-tf-module](https://github.com/sudokar/generator-tf-module)