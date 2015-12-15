# About Project
This is the tutorial project for [Jenkins Workflow in 5 Minutes](http://itechet.blogspot.co.uk/2015/12/jenkins-workflow-in-5-minutes.html).

# Quick Run
Make sure you have Vagrant 1.7 or above installed.

Then configure `jenkins-vm` and `tomcat-vm` following the README files.

To start the VMs, run
```
$ cd jenkins-vm
$ vagrant up
```
and
```
$ cd tomcat-vm
$ vagrant up
```

and you can open a browser at `192.168.2.3:8080` to verify that Tomcat has started, and `192.168.2.4:8080` to check that Jenkins is running.

For how to configure the `workflow-demo-01` job, please refer to the tutorial.
