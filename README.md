nomad-actions
=============

Only install/setup Nomad client.

Usage
-----

```yml
steps:
  - name: Setup Nomad
    uses: rluisr/nomad-actions@v1.0.0
    with:
      addr: "https://nomad.nomad.nomad"

  - name: Deploy
    run: |
      nomad job run job.hcl
```

Params
------

| Name      | Required | Description                                    |
|-----------|----------|------------------------------------------------|
| addr      | yes      | Address of the nomad server                    |
| token     | no       | Token used to authenticate with a Nomad server |
| http_auth | no       | Basic Authentication for a Nomad server        |
| version   | no       | Nomad version. If empty, used latest version   |

Locally test
------------

`$ act`