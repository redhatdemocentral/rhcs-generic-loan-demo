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
Should your local network DNS not handle the resolution of the above address, giving you page not found errors, you can apply the
following to your local hosts file:

```
$ sudo vi /etc/hosts

# add host for CDK demo resolution.
10.1.2.2   rhcs-genericloan-demo.10.1.2.2.xip.io    rhcs-genericloan-demo.10.1.2.2.xip.io
```

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


Supporting Articles
-------------------
- [Red Hat JBoss BPM Suite - Generic Loan Demo with Signal Event] (http://www.schabell.org/2014/05/redhat-jboss-bpmsuite-generic-loan-signal-event.html)

- [Red Hat JBoss BPM Suite - Automated Lending with a Generic Loan Demo] (http://www.schabell.org/2013/11/jboss-bpm-suite-automated-lending-generic-loan-demo.html)


Released versions
-----------------
See the tagged releases for the following versions of the product:

- v1.0 - JBoss BPM Suite 6.3.0 on JBoss EAP 6.4.7 with generic loan demo t installed on Red Hat CDK using OpenShift Enterprise image.

![Loan Process](https://github.com/redhatdemocentral/rhcs-generic-loan-demo/blob/master/docs/demo-images/rhcs-generic-loan-demo.png?raw=true)

![Loan Pod](https://github.com/redhatdemocentral/rhcs-generic-loan-demo/blob/master/docs/demo-images/rhcs-generic-loan-pod.png?raw=true)

![Loan Build](https://github.com/redhatdemocentral/rhcs-generic-loan-demo/blob/master/docs/demo-images/rhcs-generic-loan-build.png?raw=true)

