Concoure pipeline - Create a BOSH release tarball and save to S3
================================================================

Creates a dev release of a BOSH release from its git repo and uploads to S3 as a tarball.

![](http://cl.ly/image/1V1P3f3g1Y1S/pipeline.png)

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
