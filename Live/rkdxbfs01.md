# AEDXB-Ref-Diagram-FileTopology

This document displays a diagram of the file server \ file access topology at the AEDXB site.

#### Notes
None.

---

### Server Diagram  

![FileDiagram](./Media/AEDXB-Ref-Diagram-FileTopology/AEDXB-Ref-Diagram-FileTopology.png)


#### Notes
1. Storage is provided via iSCSI connections from: AEDXBNAS04 to both cluster nodes: AEDXBFS01A and AEDXBFS01B  
2. The Storage is presented via the cluster (AECLUSTER1) to end users using the Cluster Client Access Point name: \\\AEData  
3. The client accesses the file share via DFS-n targets, *not* via the \\\AEData UNC.  
4. The data stored on AEData is backed up to local disk (iSCSI Storage presented by AEDXBNAS04) on Azure Backup Server: AEDXBAZB01 to enable fast restores.  
5. The Backed-up data on the local storage on AEDXBAZB01 is then backed up nightly off-site to Azure cloud storage.  




---
### Related Documents
All AEDXB documents.
 
---
### Document Author(s)
**Original Creator:** OH
**Date:** 21-Sep-2018
  
