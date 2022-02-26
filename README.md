nomad-actions
=============

Only install/setup Nomad client.

Usage
-----

```yml
steps:
  - name: Setup Nomad
    uses: rluisr/nomad-actions@master

  - name: Deploy
    run: |
      nomad job run job.hcl
    env:
      NOMAD_ADDR: "https://nomad.nomad"
      NOMAD_HTTP_AUTH: "basic:auth"
    # See about environment variables https://www.nomadproject.io/docs/commands
```

Params
------

| Name      | Required | Description                                    |
|-----------|----------|------------------------------------------------|
| version   | no       | If empty, used latest version                  |

Locally test
------------

`$ act`