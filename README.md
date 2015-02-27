OpenStack Census
================

Tools for enumerating OpenStack resources of many types
(instances, floating IPs, security groups, etc.).

Keystone and Tenants
--------------------

The Keystone API is normally used to get information about tenants;
the non-authentication parts of the API may be blocked for security
(even for administrators; regular accounts rarely if ever have access).
So that these tools can be used by regular OpenStack users,
and by administrators in deployments with extra security restrictions,
a limited subset of the Keystone API is provided using static files,
notably a ``TENANTS`` file that contains tenant (project) IDs and names,
one pair per line and sorted by ID for better revision tracking.
