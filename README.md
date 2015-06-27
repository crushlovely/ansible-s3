# Ansible Role: Creates S3 Buckets

Creates one or more s3 buckets and configgures them with CORS and Makes them public.  This role also installs the AWSCLI to properly configure the buckets

## Installation

``` bash
$ ansible-galaxy install https://github.com/crushlovely/ansible-s3.git
```
## Variables

You will want to fill all these in before running the role.

``` yaml
app_name: test
server_env: qa
access_key: ""
secret_key: ""
bucket_name:
  - ""
```
You can also add a vars folder to your project folder and have your variables served by adding them to a file and calling it in your playbook.

```yaml
- hosts: localhost
...
  vars_files:
    - vars/default_vars.yml
...
```
## Usage

Once this role is installed on your system, include it in the roles list of your playbook.

``` yaml
- hosts: localhost
  connection: local
  gather_facts: True
  roles:
    - ansible-s3
```

## Dependencies

None

## License

MIT