# CI-CD Pipeline using AWS CodeCommit, AWS CodeBuild, and AWS CodePipeline

The example AWS CloudFormation template used in our May 2019 Webinar and Chicago Summit. This spins up a CodeCommit repo, a CodeBuild environment, and wires it all together with a CodePipeline

Consider this a starting point for a robust, mature pipeline.

## This template will not work if you use it as is

This template has scoped down permissions for CodeBuild and CodePipeline. The following resources contain those permissions:

* CodeBuildServiceRole
* CodePipelineServiceRole

For ease of editing, I've moved these items to the top of the `Resources` section.

## This template deploys to production without any reservation

If you're interested in doing a different approach, consider changing `            ActionMode: "CREATE_UPDATE"` in the "Deploy" category.

The different action modes are [here](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline-action-reference.html#w2ab1c13c13b9)