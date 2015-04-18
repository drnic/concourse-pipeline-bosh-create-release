Concoure pipeline - Create a BOSH release tarball and save to S3
================================================================

Example `credentials.yml`:

```yaml
aws-bosh-init-bucket: my-bucket
aws-access-key-id: ACCESS
aws-secret-access-key: SECRET
aws-region-name: us-east-1
```

```
fly c -c pipeline.yml --vars-from credentials.yml \
  --var git-bosh-release-branch=develop \
  --var git-bosh-release=https://github.com/concourse/concourse
```
