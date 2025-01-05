# Release Image Reusable Workflow

## Inputs

```yaml
- uses: jmeridth/reusable-workflows/.github/workflows/release.yml@main
  with:
    # Image name, usually owner/repository (jmeridth/reusable-workflows)
    image-name: ${{ github.repository }}
    # Full tag of the image, usually the version (v1.0.0)
    full-tag: v1.0.0
    # Short tag of the image, usually the major version (v1)
    short-tag: v1
  secrets:
    # The GitHub token to use
    github-token: ${{ secrets.GITHUB_TOKEN }}
    # Image repository url
    image-registry: ${{ secrets.IMAGE_REPOSITORY_URL }}
    # Image repository username
    image-registry-username: ${{ secrets.IMAGE_REPOSITORY_USERNAME }}
    # Image repository password
    image-registry-password: ${{ secrets.IMAGE_REPOSITORY_PASSWORD }}
```

## Outputs

None