## Alluxio Service for Ambari 2.5 (HDP 2.6)

Alluxio v 1.5.0 - Deploys on HDP 2.6


Install, start/stop, status, service check functional


**1. Clone the service into the dir for the Stack you are running in Ambari**

**- Adding Alluxio to a HDP 2.6 Cluster**

```
# Clone the service deployer
git clone https://github.com/chuyqa/alluxio-ambari-service /var/lib/ambari-server/resources/stacks/HDP/2.6/services/ALLUXIO

# Acquire the alluxio source and copy to your stack dir
aws s3 cp s3://bdap-private-artifacts/third-party/alluxio-1.5.0-hadoop-2.6-bin.tar.gz /var/lib/ambari-server/resources/stacks/HDP/2.6/services/ALLUXIO/package/files/

ambari-server restart

```


**2. Add service via Ambari ui**



**3. Assign a Alluxio Master And Worker nodes.**

By default the master will also run a worker 


Once Service is started, you may access Alluxio Master Web UI on ***alluxio.master.hostname*:19999**

**Future Work:**
Use non-root user 
defaultFS url
Metrics
Fix status check on start
Clean up & Expand alluxio-env
