<div align="right"><img alt="Smoke testing in progress" src="smoke.png"></div>

# smoketests

Some simple smoketests that can be run by Ansible to verify a site is loading.

## Requirements

none

## Role Variables

optional (see Defaults)

## Dependencies

none

## Examples

* Usage

```
    - hosts: servers
      roles:
         - smoketests
```

* Defaults

If you don't define any variables, this playbook will use the defaults found in `defaults/main.yml`

```
smoketests_host: "{{ ansible_fqdn }}"
smoketests_path: "/"
smoketests_port: "443"
smoketests_status: "200"
smoketests_content: "Copyright"
smoketests_protocol: "https"
```

* Override

If you want to override a default variable, pass it as a parameter to the role:

```
roles:
   - { role: smoketests, smoke_path: "/solr" }
```

## License

[BSD 2-Clause](https://github.com/philcryer/smoketests/blob/master/LICENSE)

## Author Information

[philcryer](https://github.com/philcryer)

Thanks
