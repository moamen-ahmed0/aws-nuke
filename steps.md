# AWS Nuke Commands

## Check Config
```bash
aws-nuke explain-config -c config.yaml   # View summary
aws-nuke resource-types                  # List types
```

## Dry Run (Safe)
```bash
aws-nuke run -c config.yaml  # Preview only
```

## Delete (DESTRUCTIVE!)
```bash
aws-nuke run -c config.yaml --no-dry-run  # Deletes all!
```

## Options
```bash
aws-nuke run -c config.yaml --region us-east-1              # Single region
aws-nuke run -c config.yaml --exclude IAMUser --exclude IAMGroup  # Skip resources
```

## Account Info
- ID: 307946672811
- Alias: aws-nuke-personal-account-307946672811
- Protected: admin, AdminGroup
