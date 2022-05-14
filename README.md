# keycloak-config-action
GitHub Action for [`adorsys/keycloak-config-cli`](https://github.com/adorsys/keycloak-config-cli)

## Usage

```yaml
steps:
  - name: Import Keycloak realm
    uses: klotztech/keycloak-config-action@18.0.0
    with:
      url: http://keycloak.example.com:8080
      username: admin
      password: password
      files: src/keycloak-realm.json
```

## Arguments
The following arguments are available:

| Input        | Description                                                       | Default value  |
| ------------ | ----------------------------------------------------------------- | -------------- |
| url          | URL of a Keycloak server                                          | Required       |
| username     | Username used to import config                                    | Required       |
| password     | Password used to import config                                    | Required       |
| login-realm  | Realm used to log in                                              | `master`       |
| files        | Location of config files (URL, file path, or Ant-style pattern)   | `/config`      |
| availability-check-enabled | Wait until Keycloak is available                    | `false`        |
| availability-check-timeout | Wait timeout for keycloak availability check        | `120s`         |
