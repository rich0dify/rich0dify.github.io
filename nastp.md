# NetApp Course NASTP

#### Read up on

* Seven Mode
* pNFS
* SVM

#### Notes (Day 1)

* Unified adapters (UTA), both FC16/10G
* AFF = All Flash Fabric Attached Storage
* Dynamic Virt Engine - easily move data around
    * Files and LUNs
    * Logical Layer - FlexVol volumes
    * Physical Layer - Aggregate/RAID Groups
* RAID 4 - no rebalance, RAID-DP is RAID4 with double parity, RAID-TEC, triple parity with erasure coding with larger drives and can support 28 drives in a RAID set
* Aggregate composed of RAID groups that contain LUNs or arrays
* FlexArray SV can be put into an Aggregate
* Agg type aggr0 - needed
* Data agg - don't/can't mix disk types
* ADP Advanced Disk Partitioning increases efficiency
* ADP v2 - partitions disks for parity
* Flash Pool Aggregate - caches, doesn't tier
* NFS > iSCSI, same performance, better dedupe, less mgmt 
* WAFL FS (Write Anywhere File Layout) 
* Flash Cache - controller lvl
* Flash Pool - storage lvl
* FAS2600 Flash Cache as standard
* SnapRestore - like "Previous Versions" for FAS/NFS etc.
* Self encrypting drives, unique data enc key, fips lvl2 or aes256 only on select disks
* NetApp Vol Enc use onboard or external key mgr 
    * Free, use all the time - can be used with compaction etc.
* OnCommand System Manager - auto setup of various applications/platforms
* OnCommand Shift - VM Converter, basically.
* CPOC - Design Slaves