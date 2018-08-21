# mage-meta-vh

Ansible role to reduce the complexity of defining all configuration options for a mass virtual hosting environment.
As for now, this role simplifies configuration of

- mage-apache
- mage-vsftpd

by:

1. creating vsftpd user with {{ user }}, {{ pass }} credentials
2. creating the docroot for domain {{ fqdn }}
3. setting up apache configuration for the {{ fqdn }}
4. binding the docroot of {{ fqdn }} to all vsftpd users with access to {{ fqdn }}

## Testing and debugging

Use the `-v` switch to increase verbosity. This will trigger debug functions to display the intermediate products
of this role.