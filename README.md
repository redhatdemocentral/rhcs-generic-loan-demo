App Dev Cloud with JBoss Generic Loan Demo
==========================================
This demo is to install JBoss BPM Suite Generic Loan Demo in the Cloud based on leveraging the Red Hat 
Container Development Kit (CDK) and the provided OpenShift Enterprise (OSE) image. It delivers a fully 
functioning JBoss BPM Generic Loan example containerized on OSE.

This demo is a financial simulation for getting a long and features BPM with human task integration,
rule integration and an example use of a signal.


Install on Red Hat CDK OpenShift Enterprise image
-------------------------------------------------
1. First complete the installation and start the OpenShift image supplied in the [cdk-install-demo](https://github.com/redhatdemocentral/cdk-install-demo).

2. Install [OpenShift Client Tools](https://developers.openshift.com/managing-your-applications/client-tools.html) if you have not done so previously.

2. [Download and unzip this demo.](https://github.com/redhatdemocentral/rhcs-travel-agency-demo/archive/master.zip)

3. Add products to installs directory.

5. Run 'init.sh' or 'init.bat' file. 'init.bat' must be run with Administrative privileges.

6. Login to start exploring a generic loan project:

    [http://rhcs-genericloan-demo.10.1.2.2.xip.io/business-central](http://rhcs-genericloan-demo.10.1.2.2.xip.io/business-central)
    ( u:erics / p:bpmsuite1! )


Notes
-----
This project can be installed on any OpenShift platform, such as OpenShift Container Platform.
It's possible to install it on any available installation by pointing this installer to an OpenShift IP address:

```
  $ ./init.sh IP
```

-----

If for any reason the installation breaks or you want a new installation, just remove the project entry in the OpenShift console and
re-run the installation.

Should your local network DNS not handle the resolution of the above address, giving you page not found errors, you can apply the
following to your local hosts file:

```
$ sudo vi /etc/hosts

# add host for OCP demo resulution
192.168.99.100   rhcs-genericloan-demo.192.168.99.100.xip.io
```

----

The demo covers the following aspects:
 - Business process definition
 - Guided Rule definition
 - Rules definition (DLR format)
 - Forms definition (for both process, to collect the input parameters, and user task)
 - Data models (using Date Modeler)
 - Helper jar to pre-load with five process instances in various states.

The following values can be used (in process form) for testing:
 - Applicant: Your Name
 - Age: 21
 - Income: 2000
 - Amount: 10010    (auto rejected if value under 10k)
 - Period (in months): 24

Any user tasks have automated task reassignment back into the group should a task not complete within a minute. Note that the entire demo is running default in memory, restart server, lose your process instances, data, monitoring history. 

-----


Supporting Articles
-------------------
- [Painless Containerized JBoss Generic Loan Processing on OpenShift](http://www.schabell.org/2016/05/painless-containerized-jboss-generic-loan-processing-openshift.html)

- [Red Hat JBoss BPM Suite - Generic Loan Demo with Signal Event] (http://www.schabell.org/2014/05/redhat-jboss-bpmsuite-generic-loan-signal-event.html)

- [Red Hat JBoss BPM Suite - Automated Lending with a Generic Loan Demo] (http://www.schabell.org/2013/11/jboss-bpm-suite-automated-lending-generic-loan-demo.html)


Released versions
-----------------
See the tagged releases for the following versions of the product:

- v1.3 - JBoss BPM Suite 6.4.0 and JBoss EAP 7.0.0 with generic loan demo installed on any given OpenShift installation and loading mulitple projects.

- v1.2 - JBoss BPM Suite 6.3.0 on JBoss EAP 6.4.7 with generic loan demo running on any given OpenShift installation and port forwarding for git repo access configured.

- v1.1 - JBoss BPM Suite 6.3.0 on JBoss EAP 6.4.7 with generic loan demo installed on Red Hat CDK.

- v1.0 - JBoss BPM Suite 6.3.0 on JBoss EAP 6.4.7 with generic loan demo installed on Red Hat CDK using OpenShift Enterprise image.

![Loan Process](https://github.com/redhatdemocentral/rhcs-generic-loan-demo/blob/master/docs/demo-images/rhcs-generic-loan-demo.png?raw=true)

![Loan Pod](https://github.com/redhatdemocentral/rhcs-generic-loan-demo/blob/master/docs/demo-images/rhcs-generic-loan-pod.png?raw=true)

![Loan Build](https://github.com/redhatdemocentral/rhcs-generic-loan-demo/blob/master/docs/demo-images/rhcs-generic-loan-build.png?raw=true)

![Cloud Suite](https://github.com/redhatdemocentral/rhcs-generic-loan-demo/blob/master/docs/demo-images/rhcs-arch.png?raw=true)

