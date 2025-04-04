# Ansible Role: OpenSCAP

This role applies the [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks) Server Level 2 recommendations on RedHat, Amazon Linux and Ubuntu on your target host(s).

> [!IMPORTANT]
> This role is still in active development. There may be unidentified issues and the role variables may change as development continues.

## Requirements

TBC

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
|||

## Dependencies

None

## License

MIT

## Author Information

This role was created in 2025 by [Yamkela (hakkutu-en)](https://github.com/hakkutu-en)
