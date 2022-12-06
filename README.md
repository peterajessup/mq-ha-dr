# cp4idemomq

This repository is to be used for creating an MQ Queue Manager on OCP, version 4.x.x, with IBM's Cloudpak for Integration Installed (verison 2021.1.1 or higher).

The artifacts include an MQ QueueManager Object Custom resource definition and
a route object associated with the channel created for access to the queue manager from outside the cluster, as well as an MQSC source yaml used to create a config-map object used for configuring the queue manager. 

In addition, a tls key and cert is provided for the queue manager's keystore, and a secret is created 
using these artifacts. These files should also be used to create a keystore for the MQ client to connect with, for simplicity.
Alternatively you can fork this repository and use your own certs and keys.

A separate persistent volume claim definition is included for use with thh Regional DR capability of Red Hat ACM, still in tech preview as of 2022/11.

To setup the Regional DR capability, see the following:

https://access.redhat.com/documentation/en-us/red_hat_openshift_data_foundation/4.10/html/configuring_openshift_data_foundation_for_regional-dr_with_advanced_cluster_management/index



