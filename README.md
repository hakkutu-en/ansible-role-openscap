# Ansible Role: OpenSCAP

This role applies the [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks) Server Level 2 recommendations on RedHat, Amazon Linux and Ubuntu on your target host(s).

> [!IMPORTANT]
> This role is still in active development. There may be unidentified issues and the role variables may change as development continues.

## Requirements

If you want to use this role, you will need to use a supported version of Ansible Core. Ansible Lint and Ansible Molecule are used if you want to contribute to this role.

* This role is developed and tested with [maintained](https://docs.ansible.com/ansible/devel/reference_appendices/release_and_maintenance.html) versions of Ansible core and Python.
* [Ansible Lint](https://ansible.readthedocs.io/projects/lint/installing/) is used to lint the role for both Ansible best practices and potential Ansible/YAML issues.
* [Ansible Molecule](https://molecule.readthedocs.io/en/latest/installation.html) is used to test the various functionalities of the role.

## Role Installation

This role can be installed via either Ansible Galaxy (the Ansible community marketplace) or by cloning this repo. Once installed, you will need to include the role in your Ansible playbook using [the `roles` keyword, the `import_role` module, or the `include_role` module](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_reuse_roles.html#using-roles).

### Ansible Galaxy

To install the latest stable release of the role on your system, use:

``` bash
ansible-galaxy install hakkutu-en.openscap
```

Alternatively, if you have already installed the role, you can update the role to the latest release by using:

``` bash
ansible-galaxy install -f hakkutu-en.openscap
```

To use the role, include the following task in your playbook:

``` yaml
- name: "Apply CIS Benchmark Server Level 2"
  ansible.builtin.include_role:
    name: "hakkutu-en.openscap"
```

### Git

To pull the latest release of the role from GitHub, use:

``` bash
git clone https://github.com/hakkutu-en/ansible-role-openscap.git
```

To use the role, include the following task in your playbook:

``` yaml
- name: "Apply CIS Benchmark Server Level 2"
  ansible.builtin.include_role:
    name: "</path/to/repo>"
```

## Role Variables

This role has multiple variables, the defaults variables are found at **[`defaults/main.yml`](/defaults/main.yml)**. See below variables and their descriptions:

|Name|Description|
|----|-----------|
|[`file_owner`](/defaults/main.yml#L3)|The owning user of role content|
|[`file_group`](/defaults/main.yml#L4)|The owning group of role content|
|[`directory_mode`](/defaults/main.yml#L5)|Permission set for directories|
|[`file_mode`](/defaults/main.yml#L6)|Permission set for files|
|[`tmp_directory`](/defaults/main.yml#L9)|User specifc temporary directory|
|[`scap_package_name`](/defaults/main.yml#L12)|Name of scap package based on OS Family|
|[`scap_content_version`](/defaults/main.yml#L15)|The release version for [ComplianceAsCode](https://github.com/ComplianceAsCode/content) content|
|[`scap_content_file`](/defaults/main.yml#L16)|The release assest file name from [ComplianceAsCode](https://github.com/ComplianceAsCode/content/releases)|
|[`scap_content_url`](/defaults/main.yml#L17)|The URL markup for downloading [ComplianceAsCode](https://github.com/ComplianceAsCode/content/) content|
|[`sudoers_base_directory`](/defaults/main.yml#L20)|The base directory where sudoers file is located|
|[`sudoers_filename`](/defaults/main.yml#L21)|The file name for sudo configuration|
|[`scap_execution_parameters`](/defaults/main.yml#L22)|The SCAP parameters used to run the script or playbook for application|

## Dependencies

None

## License

MIT

## Author Information

This role was created in 2025 by [Yamkela (hakkutu-en)](https://github.com/hakkutu-en)
