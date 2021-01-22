#  Harrison.ai Cloud Engineering Best Practices - Terraform

##  General

- Use environments in discrete folders, not workspaces, to separate environments
  - Use symlinks wherever possible to avoid repetition.
- Repos should use the 3 Musketeers Pattern, https://3musketeers.io/docs/patterns.html
- Backend:
  - S3 with optional DynamoDB locking
  - Stored in same account as deployed infrastructure
  - Terraform State key naming convention: `<repo>/<stage>/<environment>/tfstate`


### Terraform Syle Guide

Coming soon...


## Git Repo directory structure:

(incomplete)
(see also cookiecutter)

```
.
├── .env
├── .gitignore
├── Makefile
├── docker-compose.yml
├── envvars.yml
└── tf
    ├── modules
    │   └── module-one
    │       ├── main.tf
    │       ├── outputs.tf
    │       └── variables.tf
    ├── stage-one
    │   ├── dev
    │   └── prod
    └── stage-two
        ├── dev
        └── prod
```
