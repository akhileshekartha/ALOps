# Change Log
All notable changes to the "ALOps" extension.

## [v1.421] - 2019-06-24
- All PS1 files are CodeSigned for beter compatibility with standard powershell restrictions
- ALOpsAppClean: Add 'sync_mode' picklist parameter (Add/Clean/Development/ForceSync)
- ALOpsAppClean: enable for use in docker containers, use_docker parameter
- ALOpsAppTest: DisableNameChecking when importing Microsoft.Dynamics.Nav.Ide to avoid false warnings in pipeline
- ALOpsDockerRemove: added boolean parameter 'print_logs', default enabled. Prints logs on container remove.
- ALOpsDockerStart: Add -ltsc2019 or -ltsc2016 to Docker Image depending on OS
- ALOpsDockerStart: added parameter 'encryption_key', link a secret downloadable Url of the Encryption Key.
- ALOpsDockerStart: container can now be connected to Azure SQL Database
- ALOpsDockerStart: container can now be started based on a SQL BAK file via parameter 'sql_backup_file'
- ALOpsDockerStart: new default value for memory_gb parameter = '-1' (unlimited memory)
- ALOpsDockerStart: Print all docker parameters used for RUN command
- ALOpsFobImport: Added parameter for NAV Server Instance name
- ALOpsFobImport: allow for multiple FOB files to be imported in a single step, parameter 'filePath' can contain a filter like '.fob/*.fob'
- ALOpsFobImport: DisableNameChecking when importing Microsoft.Dynamics.Nav.Ide to avoid false warnings in pipeline
- ALOpsFobImport: integrate SQL-Database authentication for SQL mixed mode or Azure SQL
- ALOpsLicenseImport: Print flf license information before import
- ALOpsSaaSGetExtensions: new Task in preview mode, first of the SaaS enabled tasks. Displays the extensions installed in Business Central SaaS
- Templates: Corrected the version on the PublishTestResults step to Version 2, PublishTestResults@2

## [v1.420] - 2019-06-16
- Added YAML templates for AL Projects: https://dev.azure.com/HodorNV/ALOps%20Templates
- ALOpsAppCompiler: Added boolean parameter 'download_test_symbols' for enabling explicit Test-Package download
- ALOpsAppCompiler: Added parameter 'al_analyzer', a comma separated list of Analyzers. Example: PerTenantExtensionCop,UICop,CodeCop
- ALOpsAppCompiler: Automatically add AssemblyProbingPath if projects contains external controls
- ALOpsAppSign: The PFX password should be linked to the environment variable 'pfx_password'
- ALOpsAppTest: added Auto-Retry on the "Warm-up" step for the Test-Client
- ALOpsAppTest: Added boolean parameter 'import_testtoolkit', can be used to skip the import of the default test-suite-objects.
- ALOpsDockerStart: Added multi-line parameter 'docker_parameters', these will be added to the [docker run] command
- ALOpsDockerStart: Removed 'No container found' message when not working with Fixed-Docker-Tags
