Experitest - Reporter ansible role
=========

This role will install \ uninstall cloud server for windows, linux and mac os hosts

Requirements
------------

This role assumes that you have postgresql server already install.<br>
Supports windows, linux and mac os hosts only.

Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| state | should the application be present or absent | present, absent | present | no |
| app_version | application version to install | string | 12.8.1304 | no |
| server_port | port number for the server | number | 8084 | no |
| extra_application_properties | additional props to be override in application.properties file | dict | {} | no |
| extra_java_options | extand java options | array of strings | [] | no |
| db_connection_string | connection string to postgres | string | jdbc:postgresql://localhost:5432/reporter | no |
| db_username | username for db connection | string | postgres | no |
| db_password | password for db connection | string |  | yes |
| installation_folder | the folder in which the applcation will be installed | string | for mac: /Applications/Experitest/reporter-version <br> for windows: C:\\Experitest\\reporter-version <br> for linux: /opt/Experitest/reporter-version | no |
| jmx_port | port number for jmx inspection | number | 51238 | no |
| java_version | java jre version to install | string | 1.8.0_181 | no |
| custom_download_url | custom url to download the installation from (zip format) | string |  | no |
| start_after_install | should application start after installation is completed | boolean | True | no |
| clear_temp_folder | remove temp folder after installation | boolean | False | no |
| clear_before_install | removing old installation before installing new version | boolean | False | no |
| reporter_data_folder | the default data folder path for the reporter | string | for mac: /Library/Application Support/Experitest/reporter/uploads <br> for windows: C:\\ProgramData\\Experitest\\Reporter\\uploads <br> for linux: /var/lib/Experitest/reporter/uploads | no |
| kill_notepad | kill notepad/notepadd++ apps if opened | boolean | False | no |

Example Playbook
----------------

#### [see working example](/example)
