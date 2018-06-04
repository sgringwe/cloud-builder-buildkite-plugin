# cloud-builder, a buildkite-plugin

Submits builds to Google Cloud Builder, and shows log output with result.

Example usage:

```
- name: ":gcloud: Build App Image"
    agents:
      queue: default
    plugins:
      sgringwe/cloud-builder#be0dccd:
        auth_file: /path/to/service_account_json_key
        service_account: your_account@yourproject.iam.gserviceaccount.com
        project: yourproject
        config_file: cloudbuild.test.yaml # Defaults to 'cloudbuild.yaml'
```

## Requirements

Requires an installed `gcloud` library
