# Role Name: awx_organization

This role manages AWX organizations.

## Requirements

- Python >= 2.7
- AWX.AWX collection
  - To install it, use: `ansible-galaxy collection install awx.awx`
- Access to AWX instance

## Role Variables

```yaml
awx_controller_host:        # AWX host URL
awx_controller_username:    # AWX admin username
awx_controller_password:    # AWX admin password

awx_credentials:
  name:                     # Name of you Organization
  description:              # Description of Organization
  state:                    # State of Organization - defaults to present
```

## Example Playbook of adding an Organization

```yaml
- hosts: localhost
  roles:
    - role: awx_organization
      vars:
        awx_organizations:
          - name: SixteenOne
            description: SixteenOne Organization
            state: present
```

## License
MIT

## Author Information
This Role was created by [SixteenOne](https://bsky.app/profile/16ne.uk)
