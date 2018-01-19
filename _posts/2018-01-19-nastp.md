---
layout: post
title:  "NetApp Shite"
date:   2018-01-19 12:58:44
categories: notes
---

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
* E-Series, cheap no frills storage for single application use, EF is high perf, low latency

## Day 2

* Get notes from Jon/Vero for the start of the day
* StorageGRID, object storage - scalable, NFS, CIFS, S3 and Swift
* OpenStack + Docker integration with E-Series, ONTAP and SolidFire
* ConfigEdge - list price checker/config
* Tech Refresh Tool - can check on existing estate and then also poruce a refresh document as to what they should buy to up them to a newer, better performing SAN
    * Uses AutoSupport
    * Checks to see if anything can be reused in new SAN
* Field Portal, pre-salesy documentation technical resources, product bulletins
* NetApp Labs on Demand, can be spun for multiple days - can also just *use* it

## NASTP Answers
Q. Which buyers are increasingly becoming the dicison makers for 3rd plat apps?
A. Line of business owners

Q. Which 2 market trends are forcing traditional IT depts to transform?
A. Cloud-Like
A. Users are bypassing IT for on-demand 

Q. What are three features of emerging datacentre?
A. Software defined storage
A. Self service
A. Automation

Q. Which NetApp technology enables you to use FAS systems running ONTAP software access data on 3rd party storage systems?
A. Flex Array

Q. Which ONTAP tech creates hybrid agg of hdd of ssd to improve?
A. Flash Pool

Q. ONTAP Select software provides which benefit?
A. Converts DAS of comodity to enterprise storage

Q. Which ONTAP feature enables admins set throughput
A. Storage QoS

Q. NetApp Volume Enc (NVE) provides which benefit?
A. Does not require purpose built self encrypting drives

Q. Which statement accurately describes an ONTAP FlexGroup volume?
A. A FlexGroup Vol is a scale-out file system that is constructed from a group of FlexVol 

Q. Which OnCommand product enables an org to use it's existing 3rd party mgmt software to manage an ONTAP env?
A. OnCommand SLM

Q. Which two benefits of OnCommand WFA?
A. enables an org to adhere to storage best practice
A. enables an org to provide storage as a service

Q. How does OnCommand Insight help a customer to efficiently provision and plan purchases?
A. Forecasting

Q. An organization uses OnCommand Inishgt it's stg infra. IOPS >20 for >20ms.
A. Creating a latency threshold policy

Q. If a drive failure occurs which feature of SANtricity rebuild
A. Dynamic Disk Pools

Q. An org is eval block stg options for bznz app. The app gen IOP intensive. Which netApp stg sys should you recommend on a budget?
A. E-Series

Q. Which three target workflows benefit from E/EF?
A. NoSQL
A. Video anal
A. B2D

Q. What are two benefits of SANtricity?
A. Provide enh snap
A. Support automated SSD cache

Q. Which 3 workloads benefit SF stg?
A. Virt
A. D&T
A. DB

Q. 3 use cases for SF?
A. STGaaS
A. DevOps
A. App Consolidation

Q. What statement describes iSCSI and FC con in SF?
A. You can access a vol through iSCSI or FC at the same time

Q. How does SF improve infra agi?
A. Dynamic addition

Q. SolidFire APi for automated mgmt 2 benefits?
A. Integration
A. Rapid deployment

Q. EF storage systems benefit apps with which 2 features?
A. Do much of data mgmt
A. do not significantly benefit from data red technique

Q. AFFAS benefit from which 2 feats?
A. Benefit from data reduction
A. Require low latency and robust data mgmt

Q. SolidFire stg sys benefit customers which want to do 2 things?
A. provide managed IT
A. consolidate infra silo

Q. FlexPod solution supports which orchestration and automation solution?
A. Cisco UCS

Q. FlexPod targets which 2 env?
A. Enterprise Apps
A. VDI

Q. FlexPod with Infra Supports which HW comp?
A UCS mini, Nexus 9k, FAS2500

Q. 3 enterprise workloads for FlexPod
A. SAP HANA, OpenStack, Hadpoop

Q. An org wants to move it's data backup to the cloud. However some gov policy restrict backup to cloud?
A. NetApp Private Storage for Cloud

Q. ONTAP Cloud software provides which benefit?
A. Enabled distro of workloads between on prem and cloud

Q. Which 3 storagegrid protos?
A. S3, Swift, CIFS

Q. An org has AFF run ONTAP9.1, SnapMirror, AltaVault 4.3. Which NetApp prod enables org  to store data in cloud?
A. SnapCenter

Q. An org wants to backup data from PDC to Cloud. The org has low cost DR want to resume op.
A. AltaVault

Q. An org is eval NetApp for apps. The apps running on VMs are on ESXi. The guest are Win/Lin.
A. Interop Matrix Tool

Q. An org is eval NetApp FAS for bznz app. Which tool enables you to identify a HW config?
A. SPM

Q. An org wants to upgrade.
A. Tech Refresh Tool

Q. Synergy enabled you to perform 3 tasks.
A. Created stg capacity mode, gen tech reports and diagrams, validate system design
