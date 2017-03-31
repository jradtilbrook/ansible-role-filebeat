# Ansible Role: Filebeat [![Build Status](https://travis-ci.org/jradtilbrook/ansible-role-filebeat.svg?branch=master)](https://travis-ci.org/jradtilbrook/ansible-role-filebeat)

This role installs and configures Filebeat 5.x for the Elastic stack.

It has only been designed to work on Ubuntu 16.04, but other Debian flavours
should also work.


## Requirements

None.


## Role Variables

The `filebeat_prospectors` is a list containing all the log files to monitor.
See the Filebeat documentation for the structure of each list element.

`filebeat_output` is a dictionary of outputs to send events to. See the
Filebeat documentation for the structure and possible outputs.

`filebeat_general_config` is the general global configuration of Filebeat. Eg.
the name, extra fields or tags to apply to each event. More info can be found in
the Filebeat documentation.

`filbeat_install_state`: This is useful for updating Filebeat to newer versions
after it has already been installed. Use `latest` to achieve this functionality.


## Resources

Documentation related to Filebeat can be found at the links below:

- [documentation](https://www.elastic.co/guide/en/beats/libbeat/current/beats-reference.html)


## Dependencies

None.

Check out my other roles on [Ansible Galaxy](https://galaxy.ansible.com/jradtilbrook)
if you are installing the entire Elastic Stack.


## Example Playbook

```yaml
- hosts: servers
  become: yes

  roles:
    - role: jradtilbrook.filebeat
```


## License

MIT
