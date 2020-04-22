# SOSREPORTER

A tool for automating the creation and collection of sos reports.

## Requirements

1. Ansible

   You need a recent version of [Ansible][].

2. An inventory

   You need an [Ansible inventory][] listing your target hosts.

## Running the playbook

To gather sosreports from your hosts:

```
ansible-playbook sosreporter.yml -i path/to/your/inventory
```

This will run `sosreport` on each host in your inventory and then copy the resulting archives into the `reports/` directory adjacent to the playbook.

## Available configuration variables

- `case_id` -- setting this will include the case id the generated filenames.

- `sosreport_flags` -- any additional flags to pass to `sosreport`


[ansible]: http://www.ansible.com/
[ansible inventory]: https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html
