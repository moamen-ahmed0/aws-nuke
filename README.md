# AWS Nuke

Tool to delete all resources in your AWS account.

## ⚠️ Warning

**This will delete ALL resources in your AWS account!** Only use on test/development accounts.

## Installation

```bash
brew install aws-nuke
```

## Setup

1. Configure AWS credentials:
   ```bash
   aws configure
   ```

2. Edit `config.yaml` with your account ID (already configured: `307946672811`)

3. Account alias is set: `aws-nuke-test-307946672811`

## Usage

**Dry run (safe - shows what would be deleted):**
```bash
aws-nuke run -c config.yaml
```
Type the account alias when prompted: `aws-nuke-test-307946672811`

**Actually delete resources:**
```bash
aws-nuke run -c config.yaml --no-dry-run
```

## Excluding Resources

Edit `config.yaml` to exclude specific resources:

```yaml
accounts:
  "307946672811":
    filters:
      S3Bucket:
        - "my-important-bucket"
      IAMUser:
        - "admin-user"
```

## More Info

- [AWS Nuke GitHub](https://github.com/rebuy-de/aws-nuke)
- [Documentation](https://ekristen.github.io/aws-nuke/)
