# Batch task control and monitoring for EOL traitbank

First time Jenkins setup

 - I'm doing Jenkins server experimentation and development on 
   varela.csail.mit.edu for now
 - I installed Jenkins on varela from 
   https://pkg.jenkins.io/debian-stable/binary/jenkins_2.190.2_all.deb
 - Initial admin password is written on installation to 
   /var/lib/jenkins/secrets/initialAdminPassword
 - In absence of HTTPS, listening for now only on 127.0.0.1.
 - For local modification(s) to /etc/default/jenkins (e.g. HTTP configuration), see 
   [here](etc-default-jenkins).
 - 'Create First Admin User' jar

Connecting to Jenkins

 - Make sure client (e.g. your GNU/Linux or MacOS laptop) is authorized 
   to connect to varela.csail.mit.edu using ssh
 - On client, set up ssh tunnel: `ssh -N -L 8080:localhost:8080 varela.csail.mit.edu`
 - On client, connect to Jenkins by browsing to http://127.0.0.1:8080/

Development

 - Use pipelines instead of freestyles to facilitate source control,
   audit, replicability, etc.
 - One github repository directory per 'job', each with its own `Jenkinsfile`
 - Job configuration information entered via the Jenkins UI seems to be stored in
   /var/lib/jenkins/jobs/{jobname}/config.xml
   which we might want to put under source control

