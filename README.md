# remote sync

- config file uses file format similar to INI, semicolons indicate comments
- repositories are specified by individual sections, eg., `[repo]`
- `[DEFAULT]` section applies to all repositories
- two section options are available: `remotes` and `filters`
- multiple remotes or filters need to be separated by commas
- trailing slashes in repository names matter

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

