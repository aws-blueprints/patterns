# Patterns

Have you ever thought `How do I do "x"` when working with Terraform in AWS? Ya?! Well, this is the place to ask those questions and (hopefully) get some answers.

### 🚧 👷 Warning - early days and still under construction 🚧

## Why?

1. To state the obvious - demonstrate how to implement various architectural patterns in AWS using Terraform
2. To demonstrate various use cases for [`terraform-aws-modules`](https://github.com/terraform-aws-modules?type=source). The examples provided in each modules `examples/` directory are great, but it's not representative of how to use the module in a real "world scenario" (what is "real" anyways?!). The `examples/` tend to become more of "testbed" for the module and not very reflective of what you would see deployed in an environment.
3. (I hate the phrase but you know I'm going to have to say it) Demonstrate "best practices". Ok, lets call them recommended practices from now on. Running tools like `tfsec`, `checkov`, `terrascan`, etc., on a module repository is never going to yield great results because scanning a module definition is nearly useless and scanning an example is not representative of anything material. Instead, we can use those tools here since the patterns provided will be more reflective of "production-like" or "real world-like" use cases.
4. How do you improve a module? By using it over and over repeatedly in various use cases - finding and smoothing out the rough edges, looking for common patterns that can be pulled into the module definition itself for better usability, identifying better default values that would improve the out-of-box experience, etc. This will also support questions raised in the module repositories - providing a valid use case that can be referenced to either help answer questions or aid in reproducing issues.

## Questions

Q: Is Terraform the only supported language? \
A: Currently, yes

Q: How do I request a pattern to be added? \
A: TBD

Q: How can I contribute? \
A: TBD

## Patterns

### Containers

- [ ] Something

### Messaging

- [ ] Fan-out: SNS(1) to SQS(n) w/ DLQ to Lambda(n:m)
- [ ] Ordered buffer: FIFO SNS(1) to FIFO SQS(1) w/ DLQ to Lambda
- [ ] Scatter-gather: Lambda(1) to SNS(1) to Lambda(n) to SQS(1) to Lambda(1) w/ DynamoDB
- [ ] SNS Routing: SNS(1) to SQS(n) w/ DLQ

### Networking

- [ ] Something
