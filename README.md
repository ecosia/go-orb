# Go (Golang) Orb [![CircleCI Build Status](https://circleci.com/gh/ecosia/go-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/ecosia/go-orb) [![CircleCI Orb Version](https://badges.circleci.com/orbs/ecosia/go.svg)][reg-page] [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://github.com/ecosia/go-orb/blob/main/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

A Go Orb for CircleCI.
This orb allows you to do common Go related tasks on CircleCI such as install Go, downloading modules, caching, etc. This repository was forked from the CircleCI repository [circleci/golang](https://github.com/CircleCI-Public/go-orb/tree/master).

## Usage

Example usage as well as a list of available executors, commands, and jobs are available on this orb's [registry page][reg-page].

## Resources

[CircleCI Orb Registry Page][reg-page] - The official registry page for this orb will all versions, executors, commands, and jobs described.  
[CircleCI Orb Docs](https://circleci.com/docs/2.0/orb-intro/#section=configuration) - Docs for using and creating CircleCI Orbs.  

## Contributing

We welcome [issues](https://github.com/ecosia/go-orb/issues) and [pull requests](https://github.com/ecosia/go-orb/pulls) against this repository!
For further questions/comments about this or other orbs, visit the Orb Category of [CircleCI Discuss](https://discuss.circleci.com/c/orbs).

### Publishing

New versions of this orb are published by having the merge commit follow the convention `[semvar:<patch/minor/major>] commit details`. Note that Circle CI relies on a API token to publish the orb, this is set as an environment variable `CIRCLE_TOKEN` in the [organisation orb-publishing context](https://app.circleci.com/settings/organization/github/ecosia/contexts/73b7b088-da89-49c0-8363-b8c4a92437a3?return-to=https%3A%2F%2Fapp.circleci.com%2Fpipelines%2Fgithub%2Fecosia%2Fgo-orb%2F82%2Fworkflows%2Fe7f2990a-9251-4c84-8770-6246f0db630b%2Fjobs%2F349) (it currently uses the ecosiabot token).

#### Troubleshooting

##### `Error: dev version has expired`

Example error message:

```
The dev version of ecosia/go@dev:alpha has expired. Dev versions of orbs are only valid for 90 days after publishing.
```

This means that the orb has not been published in the last 90 days. To fix this, publish a new version of the orb by running the script `./publish-alpha.sh` from the root of the repository (you will need the circle ci cli installed and to have created a [personal API token](https://circleci.com/account/api) then run `circleci setup` to configure the cli)

[reg-page]: https://circleci.com/orbs/registry/orb/ecosia/go
