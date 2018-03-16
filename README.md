# remote sync

- config file uses file format similar to INI, semicolons indicate comments
- repositories are specified by individual sections, eg., `[repo]`
- `[DEFAULT]` section applies to all repositories
- trailing slashes in repository names matter
- multiple options need to be separated by commas, the following options are available
	- `remotes`: (remote) destination(s)
	- `filters`: rsync filter rule(s)

# example configuration

``` 
; repository defaults
[DEFAULT]
remotes: user@192.168.1.100:~/path
default_filters: - *.tmp, - *.swp
filters: %(default_filters)s

; test repository
[repo]
repo_filter: - aux
filters: %(default_filters)s, %(build_filter)s
``` 

