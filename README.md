# AWS Terraform Module ACM Certificate
A Terraform module to create an Amazon Certificate Manager (ACM) certificate with Route 53 DNS validation.

## Variables

- `domain_name` - Primary domain name associated with certificate. Also used for the Name tag of the ACM certificate.
- `subject_alternative_names` - Subject alternative domain names.
- `hosted_zone_id` - Route 53 hosted zone ID for `domain_name`.
- `validation_record_ttl` - Route 53 record time-to-live (TTL) for validation record (default: `60`).
- `allow_validation_record_overwrite` - Allow Route 53 record creation to overwrite existing records (default: `true`).
- `tags` - A map of extra tags that is associated with the ACM Certificate.

## Outputs

- `arn` - The Amazon Resource Name (ARN) of the ACM certificate