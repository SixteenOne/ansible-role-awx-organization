# Role Name: awx_organization

This role manages AWX organizations.

## Requirements

- Python >= 2.7
- AWX.AWX collection
  - To install it, use: `ansible-galaxy collection install awx.awx`
- Access to AWX instance

## Role Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `awx_organization_name` | Name of the organization to create/manage | None |
| `awx_organization_description` | Description of the organization | "" |
| `awx_organization_state` | Desired state of the organization (present/absent) | present |
| `awx_host` | URL of the AWX/Tower instance | http://localhost |
| `awx_username` | Username for AWX/Tower authentication | admin |
| `awx_password` | Password for AWX/Tower authentication | password |
| `awx_validate_certs` | Whether to validate SSL certificates | true |

## Example Playbook of adding an Organization

```yaml
- hosts: localhost
  roles:
    - role: awx_organization
      vars:
        awx_organization_name: "My Company"
        awx_organization_description: "Primary organization for My Company"
        awx_host: "https://awx.example.com"
        awx_username: "admin"
        awx_password: "secure_password"
        awx_validate_certs: true
```

## License
MIT

## Author Information
This Role was created by [SixteenOne](https://bsky.app/profile/16ne.uk)
