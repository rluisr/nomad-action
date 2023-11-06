# nomad-actions

Only install/setup Nomad client and nomad-pack.

## Usage

```yml
steps:
  - name: Setup Nomad
    uses: rluisr/nomad-actions@master

  - name: Deploy
    run: |
      nomad job run job.hcl
      # or nomad-pack run .
    env:
      NOMAD_ADDR: "https://nomad.nomad"
      NOMAD_HTTP_AUTH: "basic:auth"
    # See about environment variables https://www.nomadproject.io/docs/commands
```

## Params

| Name          | Required | Description                   |
| ------------- | -------- | ----------------------------- |
| nomad_version | no       | If empty, used latest version |

**IMPORTANT NOTICE**

`nomad-pack` is under the preview and we can not download specified version binary.  
This actions now download `0.1.1.dev`

## Locally test

`$ act`
