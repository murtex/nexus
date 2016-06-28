Remote sync nexus
=================

### Example configuration

	; defaults
	[DEFAULT]
	remotes: user@192.168.1.100:~/path
	default_filters: - *.tmp, - *.swp
	filters: %(default_filters)s

	; repositories
	[config]

	[ves]
	build_filter: - build
	filters: %(default_filters)s, %(build_filter)s

	[diploma]
	data_filter: - *.h5, - *.csv
	filters: %(default_filters)s, %(data_filter)s

