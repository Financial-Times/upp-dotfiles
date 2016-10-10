# UPP Dotfiles

A collection of useful bash commands, variables etc.

## Usage

To use these dotfiles, simply checkout the repository somewhere suitable (i.e. `~/Code/upp-dotfiles`), and add the following to your `.bash_profile`:

```sh
. ~/Code/upp-dotfiles/.imports
```

For further customisation, it's recommended that you fork this repo.

## Commands

Here's a non-exhaustive list of commands offered by these dotfiles.

To run the Mongo CLI on the primary mongo in a given cluster:

```sh
primary_mongo $upp_tunnel_url
```

To locate authentication credentials for a cluster for use in a curl command:

```sh
curl http://upp_service_host/ -u $(auth $upp_tunnel_url)
```

To report the CoreOS version for each machine in the cluster:

```sh
coreos_version $upp_tunnel_url
```

## Variables

See [.clusters](/.clusters) for useful environment variables.
