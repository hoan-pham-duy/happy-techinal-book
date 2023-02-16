### AWS Certified DevOps Engineer Professional 2023 - Hands On!, Stephane Maare

- [Section 1: Course overview]()
- [Section 2: Code & Slides Download]()
- [Section 3: SLDC (Software Development Life Cycle) Automation]()

<details>
<summary> 4. CICD Overiew: </summary>
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
<summary>5. Reference Link: </summary>
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
    <summary>6. CodeCommit</summary>
- Version Control
- Central online git repository
- Collaborate, backup code
- AWS CodeCommit: private Git repositories
</details>
<details>
    <summary>7. CodeCommit - First Repo & HTTPs config</summary>
- 2 ways connect to CodeCommit: SSH and HTTPs
- HTTPs: create IAM Role
</details>
<details>
    <summary>8. CodeCommit - clone, add, commit, push</summary>
- Should commit appspec.yml (CodeDeploy) + buildspec.yml (CodeBuild)
</details>
<details>
    <summary>9. CodeCommit - Branches and Pull Requests</summary>
- Should have master branch, staging branch, feature branches
- git push --set-upstream ... if the current branch has no up-stream branch
- Crerate Pull Request from feature branches to master branch
</details>