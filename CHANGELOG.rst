================================
lowlydba.sqlserver Release Notes
================================

.. contents:: Topics


v1.0.0
======

Release Summary
---------------

Bumping to version 1.0.0 now that this collection is being used in production in at least one place 🎉

v0.11.2
=======

Release Summary
---------------

Bumping required dbatools version to ensure the `restore` module works on MacOS PowerShell Core (https://github.com/dataplat/dbatools/pull/8435).

v0.11.1
=======

Release Summary
---------------

Bug fixes for AlwaysOn related modules and fixing errors in some documentation examples.

Bugfixes
--------

- Fix `availability_group` module so that NUL backups can be properly taken if needed.
- Fix incorrect examples in `availability_group` module documentation.
- Fix incorrect examples in `install_script` module documentation.
- Fix incorrect examples in `spn` module documentationb.
- Fixed bugs where adding replica did not work properly for several reasons.

v0.11.0
=======

Release Summary
---------------

Adding new dbops module.

New Modules
-----------

- install_script - Runs migration scripts against a database.

v0.10.1
=======

Release Summary
---------------

Bug fix for resource_governor.

Bugfixes
--------

- Fix change detection in resource_governor module.

v0.10.0
=======

Release Summary
---------------

The first_responder_kit and tcp_port modules, along with a bump in the required dbatools version.

Minor Changes
-------------

- Update minimum required DBATools version universally to 1.1.108 to accommodate new tcp module.

New Modules
-----------

- first_responder_kit - Install/update the First Responder Kit scripts.
- tcp_port - Sets the TCP port for the instance.

v0.9.3
======

Release Summary
---------------

More change detection fixing.

Bugfixes
--------

- memory - Fix improper changed detection.

v0.9.2
======

Release Summary
---------------

Bugfixes for agent related modules that incorrectly reported change statuses.

Bugfixes
--------

- agent_job - Fix incorrectly reported change status when no change occurred.
- agent_job_schedule - Fix incorrectly reported change status when no change occurred.
- agent_job_step - Fix incorrectly reported change status when no change occurred.

v0.9.1
======

Release Summary
---------------

Bugfix!

Bugfixes
--------

- Allow agent job steps to be removed by specifying the step ID only. This is likely needed in cleanup of steps from previous job configurations.

v0.9.0
======

Bugfixes
--------

- backup - Only use blocksize when specified.

New Modules
-----------

- restore - Performs a restore operation.

v0.8.0
======

Release Summary
---------------

A few small fixes and the new 'backup' module.

Minor Changes
-------------

- Standardize use of 'database' vs 'database_name' in all documentation and options specs. Not a breaking change.

Bugfixes
--------

- Fix inability to enable an agent job schedule after it has been disabled.

New Modules
-----------

- backup - Performs a backup operation.

v0.7.0
======

Release Summary
---------------

Add module for DBA Multitool.

New Modules
-----------

- dba_multitool - Install/update the DBA Multitool suite by John McCAll

v0.6.0
======

Release Summary
---------------

Adding new SPN module

New Modules
-----------

- spn - Configures SPNs for SQL Server.

v0.5.0
======

Release Summary
---------------

CI and testing improvements, along with the final availability group module ag_replica.

Minor Changes
-------------

- Remove CI support for Ansible 2.10

New Modules
-----------

- ag_listener - Configures an availability group listener.
- ag_replica - Configures an availability group replica.

v0.4.0
======

Release Summary
---------------

Two new AlwaysOn modules and a few consistency fixes!

Minor Changes
-------------

- Test for 'Name' property for sa module after dbatools release 1.1.95 standardizes command outputs. (https://github.com/dataplat/dbatools/releases/tag/v1.1.95)

Breaking Changes / Porting Guide
--------------------------------

- All modules should use a bool 'enabled' instead of a string 'status' to control object state.

New Modules
-----------

- availability_group - Configures availability group(s).
- hadr - Enable or disable HADR.

v0.3.0
======

Release Summary
---------------

New sa module and fixes for login related modules.

Minor Changes
-------------

- Fix logic to properly pass password policy options to function in the login module.

New Modules
-----------

- sa - Configure the 'sa' login for security best practices.

v0.2.0
======

Release Summary
---------------

Code cleanup, testing improvements, new _info module!

Minor Changes
-------------

- Add DbaTools module requirement to documentation and fix missing examples. (https://github.com/lowlydba/lowlydba.sqlserver/pull/47)
- Utilize PowerShell Requires for dbatools min version needs instead of custom function. Consolidate/standardize credential setup and serialization. (https://github.com/lowlydba/lowlydba.sqlserver/pull/48)

New Modules
-----------

- instance_info - Returns basic information for a SQL Server instance.

v0.1.1
======

Release Summary
---------------

Add database tag for Galaxy

v0.1.0
======

Release Summary
---------------

It's a release! First version to publish to Ansible Galaxy.

New Modules
-----------

- agent_job - Configures a SQL Agent job.
- agent_job_category - Configures a SQL Agent job category.
- agent_job_schedule - Configures a SQL Agent job schedule.
- agent_job_step - Configures a SQL Agent job step.
- database - Creates and configures a database.
- login - Configures a login for the target SQL Server instance.
- maintenance_solution - Install/update Maintenance Solution
- memory - Sets the maximum memory for a SQL Server instance.
- nonquery - Executes a generic nonquery.
- resource_governor - Configures the resource governor on a SQL Server instance.
- rg_resource_pool - Configures a resource pool for use by the Resource Governor.
- rg_workload_group - Configures a workload group for use by the Resource Governor.
- sp_configure - Make instance level system configuration changes via sp_configure.
- sp_whoisactive - Install/update sp_whoisactive by Adam Mechanic.
- traceflag - Enable or disable global trace flags on a SQL  Server instance.
