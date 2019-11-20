# eol-batch
Batch task control and monitoring for EOL traitbank

 - Do development on varela
 - Installed Jenkins on varela from 
   https://pkg.jenkins.io/debian-stable/binary/jenkins_2.190.2_all.deb
 - Initial admin password is written on installation to 
   /var/lib/jenkins/secrets/initialAdminPassword
 - For modification(s) to /etc/default/jenkins, see
   [[etc-default-jenkins]].  (In absence of HTTPS, listening for now only on 127.0.0.1.)
 - Set up ssh tunnel as usual: `ssh -N -L 8080:localhost:8080 varela`
 - 'Create First Admin User' jar
 - Use pipelines instead of freestyles to facilitate source control,
   audit, replicability, etc.
 - Job configuration information entered via the UI seems to be stored in
   /var/lib/jenkins/jobs/{jobname}/config.xml
   which we might want to put under source control ?
