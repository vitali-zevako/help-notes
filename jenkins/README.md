##### Stop jenkins zombie job from script console
`Jenkins.instance.getItemByFullName('<job_name>').getBuildByNumber(<job_number>).finish(hudson.model.Result.ABORTED, new java.io.IOException('Aborting build'))`
##### Trigger jenkins job remotely
`curl -XPOST -u <username>:<password> <jenkins_url>:<port>/job/<job_name>/build`
##### Trigger parameterized jenkins job remotely
`curl -XPOST -u <username>:<password> <jenkins_url>:<port>/job/<job_name>/buildWithParameters`
