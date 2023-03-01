<style>
.content-header {
    color: #3996d6;
}
</style>
### AWS Certified DevOps Engineer Professional 2023 - Hands On!, Stephane Maare

- [Section 1: Course overview]()
- [Section 2: Code & Slides Download]()
- [Section 3: SLDC (Software Development Life Cycle) Automation]()
<details>
    <summary class="content-header"> 4. CICD Overiew: </summary>
+ Continous Integration
<div>
    <img src='./statics/CI_CD_useful.png' style="height: 300px;">
</div>
+ Continous Delivery:
<div>
    <img src='./statics/Continous Delivery.png' style="height: 300px;">
</div>
+ Continous Delivery vs Continous Deployment: <br />
Continous Delivery may invole a manual step to approvev a deployment <br />
Continous Deployment: Full automation <br>
+ Technology Stack for CICD:
<div>
    <img src='./statics/tech_stack_CICD.png' style="height: 300px;">
</div>
</details>
<details>
<summary class="content-header">5. Reference Link: </summary>
CodeCommit

    https://www.atlassian.com/git/tutorials/using-branches

    https://docs.aws.amazon.com/codecommit/latest/userguide/auth-and-access-control-iam-identity-based-access-control.html

    https://aws.amazon.com/blogs/devops/refining-access-to-branches-in-aws-codecommit/

    https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-notify.html

    https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-repository-email.html )

    https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-notify-lambda.html

    https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-migrate-repository-existing.html

CodeBuild

    https://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html

    https://docs.aws.amazon.com/codebuild/latest/userguide/samples.html

    https://docs.aws.amazon.com/codebuild/latest/userguide/sample-docker.html

    https://aws.amazon.com/blogs/devops/validating-aws-codecommit-pull-requests-with-aws-codebuild-and-aws-lambda/

CodeDeploy

    https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_MinimumHealthyHosts.html

    https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html

    https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html#appspec-hooks-server

    https://docs.amazonaws.cn/en_us/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html#reference-appspec-file-structure-environment-variable-availability

    https://docs.aws.amazon.com/codedeploy/latest/userguide/monitoring-cloudwatch-events.html

    https://aws.amazon.com/blogs/devops/view-aws-codedeploy-logs-in-amazon-cloudwatch-console/

    https://docs.aws.amazon.com/codedeploy/latest/userguide/monitoring-sns-event-notifications.html

    https://docs.aws.amazon.com/codedeploy/latest/userguide/deployments-rollback-and-redeploy.html

    https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-groups-configure-advanced-options.html

    https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-on-premises.html

    https://docs.aws.amazon.com/codedeploy/latest/userguide/register-on-premises-instance-iam-user-arn.html

    https://docs.aws.amazon.com/codedeploy/latest/userguide/register-on-premises-instance-iam-session-arn.html

    https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-configurations.html#deployment-configuration-lambda

    https://docs.aws.amazon.com/codedeploy/latest/userguide/reference-appspec-file-structure-hooks.html#appspec-hooks-lambda

CodePipeline

    https://docs.aws.amazon.com/codepipeline/latest/userguide/reference-pipeline-structure.html#action-requirements

    https://docs.aws.amazon.com/codepipeline/latest/userguide/best-practices.html#use-cases

    https://docs.aws.amazon.com/codepipeline/latest/userguide/actions-invoke-lambda-function.html

    https://docs.aws.amazon.com/codepipeline/latest/userguide/actions-create-custom-action.html

    https://docs.aws.amazon.com/codepipeline/latest/APIReference/API_PutJobSuccessResult.html

    https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline.html

    https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-cloudformation.html

    https://github.com/aws-samples/codepipeline-nested-cfn

    https://aws.amazon.com/blogs/devops/implementing-gitflow-using-aws-codepipeline-aws-codecommit-aws-codebuild-and-aws-codedeploy/

CodeStar

    https://docs.aws.amazon.com/codestar/latest/userguide/templates.html

Jenkins

    https://aws.amazon.com/getting-started/projects/setup-jenkins-build-server/

    https://wiki.jenkins.io/display/JENKINS/Amazon+EC2+Plugin

    https://aws.amazon.com/blogs/devops/setting-up-a-ci-cd-pipeline-by-integrating-jenkins-with-aws-codebuild-and-aws-codedeploy/

    https://wiki.jenkins.io/display/JENKINS/AWS+CodeBuild+Plugin

    https://wiki.jenkins.io/display/JENKINS/Amazon+EC2+Container+Service+Plugin

    https://wiki.jenkins.io/display/JENKINS/Artifact+Manager+S3+Plugin

    https://wiki.jenkins.io/display/JENKINS/AWS+CodePipeline+Plugin 
</details>
<details>
    <summary class="content-header">6. CodeCommit</summary>
- Version Control<br />
- Central online git repository<br />
- Collaborate, backup code<br />
- AWS CodeCommit: private Git repositories<br />
</details>
<details>
    <summary class="content-header">7. CodeCommit - First Repo & HTTPs config</summary>
- 2 ways connect to CodeCommit: SSH and HTTPs<br />
- HTTPs: create IAM Role<br />
</details>
<details>
    <summary class="content-header">8. CodeCommit - clone, add, commit, push</summary>
- Should commit appspec.yml (CodeDeploy) + buildspec.yml (CodeBuild)<br />
</details>
<details>
    <summary class="content-header">9. CodeCommit - Branches and Pull Requests</summary>
- Should have master branch, staging branch, feature branches<br />
- git push --set-upstream ... if the current branch has no up-stream branch<br />
- Create Pull Request from feature branches to master branch<br />
</details>
<details>
    <summary class="content-header">10. CodeCommit - Securing the Repository and Branches</summary>
    - Limit Pushes and Merges to Branches (eg. only Admin can merge the code to master) by attaching Policy to IAM User (eg. Deny codecommit:DeleteBranch)<br />
</details>
<details>
    <summary class="content-header">11. CodeCommit - Triggers & Notifications</summary>
    - Automation with Notifications, Triggers (connect to SNS, Lambda)<br />
    - Should create Repository tags.<br />
</details>
<details>
    <summary class="content-header">12. CodeCommit - & AWS Lambda</summary>
    - Lambda is good for automation <br />
    - Send notification to Lambda or trigger Lambda <br />
</details>
<details>
    <summary class="content-header">13. CodeBuild - Overview</summary>
    - Fully managed build service, such as Jenkins Build <br />
    - Continuous scaling (no servers to manage or provision – no build queue) <br />
    - Leverages Docker under the hood, can use your own Docker, pay as use <br />
    - Secure: Integration with KMS for encryption of build artifacts,IAM for build permissions, and VPC for network security, CloudTrail for API calls logging.
</details>
<details>
    <summary class="content-header">13. CodeBuild - Overview</summary>
    - Fully managed build service, such as Jenkins Build <br />
    - Continuous scaling (no servers to manage or provision – no build queue) <br />
    - Leverages Docker under the hood, can use your own Docker, pay as use <br />
    - Secure: Integration with KMS for encryption of build artifacts,IAM for build permissions, and VPC for network security, CloudTrail for API calls logging.
    - Source Code from GitHub / CodeCommit / CodePipeline / S3... <br />
    - Build instructions can be defined in code (buildspec.yml file) <br />
    - Output logs to Amazon S3 & AWS CloudWatch Logs <br />
    - Metrics to monitor CodeBuild statistics <br />
    - Use CloudWatch Events to detect failed builds and trigger notifications <br />
    - Use CloudWatch Alarms to notify if you need “thresholds” for failures <br />
    - CloudWatch Events / AWS Lambda as a Glue <br />
    - SNS notifications <br />
</details>
<details>
    <summary class="content-header">14. CodeBuild - First Build</summary>
    - Choose Source with reference types (branch, git tag, commit ID) to build <br />
    - Choose Manage Image or Custom image (your own Docker)
</details>