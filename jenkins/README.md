##### Cancel queue
`import hudson.model.*
import jenkins.model.Jenkins
def q = Jenkins.instance.queue
q.items.findAll { it.task.name.contains('aws-devops-root') }.each { q.cancel(it.task) }`
##### Stop jenkins zombie job from script console
`Jenkins.instance.getItemByFullName('<job_name>').getBuildByNumber(<job_number>).finish(hudson.model.Result.ABORTED, new java.io.IOException('Aborting build'))`
##### Trigger jenkins job remotely
`curl -XPOST -u <username>:<password> <jenkins_url>:<port>/job/<job_name>/build`
##### Trigger parameterized jenkins job remotely
`curl -XPOST -u <username>:<password> <jenkins_url>:<port>/job/<job_name>/buildWithParameters`
