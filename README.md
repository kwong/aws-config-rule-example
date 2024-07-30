# aws-config-rule-example

Example CloudFormation Guard definition to enforce tagging rules using AWS Config rules.


To run:
1. Install [Guard for your OS](https://docs.aws.amazon.com/cfn-guard/latest/ug/setting-up-linux.html)
2. Clone the project
3. Run the command

```sh
cfn-guard validate --rules tag-rule.guard --data resource.json
```

## Example output

```sh
FAILED rules
tag-rule.guard/default    FAIL
---
Evaluation of rules tag-rule.guard against data /Users/kangwei/Projects/aws-config-rule-example/resource.json
--
Property [/tags/Owner] in data [/Users/kangwei/Projects/aws-config-rule-example/resource.json] is not compliant with [tag-rule.guard/default] because provided value ["kangwei.wong"] did not match expected value ["/^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.[a-zA-Z]{2,}$/"]. Error Message []
--
```