# AWS-SAA-Projects

A recruiter-friendly portfolio of AWS Solutions Architect Associate (SAA) projects completed in a lab-based learning environment and translated into reproducible Infrastructure as Code.

## Why this repository exists

These projects started as guided hands-on labs in **Amazon LMS** with sandbox environments provided by **Vocareum**. The labs are excellent for learning architecture patterns quickly, but the environments are temporary and tightly controlled. This repository turns those short-lived exercises into reusable, production-minded project artifacts that can be reviewed by recruiters and hiring managers.

## Learning environment: Amazon LMS + Vocareum

### Amazon LMS
- Structured learning path for AWS SAA topics (networking, compute, storage, IAM, monitoring, and architecture design).
- Guided lab instructions and architecture objectives.

### Vocareum lab environment
- Time-boxed AWS sandbox accounts.
- Preconfigured credentials and guardrails.
- Great for experimentation, but not ideal for long-term portfolio proof unless work is documented and codified outside the lab session.

## Common limitations of the labs

Working through LMS/Vocareum labs typically introduces constraints such as:

- **Ephemeral accounts/sessions**: resources are deleted when sessions end.
- **Limited permissions**: IAM restrictions prevent full account-level administration.
- **Budget and service quotas**: strict limits on instance sizes, regions, and advanced services.
- **Manual, click-heavy workflow**: console steps are hard to version and repeat.
- **Weak portability**: reproducing the same architecture later is slow and error-prone without code.

## How Terraform addresses those limitations

Terraform is used as the bridge between lab learning and real-world engineering practice:

- **Reproducibility**: entire stacks can be recreated from code in any allowed AWS account.
- **Version control**: infrastructure changes are tracked with commit history and review.
- **Consistency**: standardized variables, modules, and outputs reduce configuration drift.
- **Faster rebuilds**: when a lab expires, the same architecture can be provisioned again quickly.
- **Professional signal**: demonstrates IaC fluency, system thinking, and DevOps workflow maturity.

## Project portfolio map

The projects in this repository represent end-to-end SAA-aligned architecture patterns, including combinations of:

- **Networking**: VPC design, subnets, route tables, NAT/public-private segmentation.
- **Compute**: EC2-based application tiers, autoscaling concepts, and secure access patterns.
- **Storage**: S3 for static assets, backups, and lifecycle-aware storage design.
- **Database**: managed relational/non-relational service integration patterns.
- **Security**: IAM roles/policies, security groups, least-privilege access design.
- **Observability**: CloudWatch metrics/logging and operational visibility.

> As this portfolio evolves, each project should include its own folder with architecture notes, Terraform code, and deployment instructions.

## How to present this to recruiters and hiring managers

This repository is designed to communicate more than “I followed a lab.” It demonstrates:

- Ability to convert guided exercises into repeatable infrastructure definitions.
- Understanding of AWS architectural tradeoffs rather than one-off console actions.
- Practical use of Git-based collaboration and change tracking.
- Readiness to contribute to cloud/platform teams that rely on Infrastructure as Code.

## Suggested project structure (recommended)

For each project, use a structure like:

```text
projects/
  project-name/
    README.md              # problem statement, architecture, and outcomes
    main.tf                # core resources
    variables.tf           # input variables
    outputs.tf             # useful outputs
    terraform.tfvars.example
    diagrams/              # architecture visuals
```

## Usage notes

1. Install Terraform and configure AWS credentials for a non-lab account.
2. Initialize and validate each project:
   - `terraform init`
   - `terraform validate`
   - `terraform plan`
3. Apply only in accounts where you are authorized to create resources.

## Audience

- **Recruiters**: quick evidence of real AWS project depth beyond certificates.
- **Hiring managers**: concrete proof of IaC capability, cloud fundamentals, and engineering communication.
- **Technical interviewers**: artifacts for architecture and implementation deep-dives.

---

If you are reviewing this repository for hiring, the key takeaway is that each lab concept is intentionally transformed into reproducible, reviewable cloud infrastructure code suitable for team environments.
