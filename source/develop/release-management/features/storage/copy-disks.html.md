---
title: Copy Disks
authors: tjelinek
wiki_title: Features/Copy Disks
wiki_revision_count: 1
wiki_last_updated: 2015-05-15
---

# Copy Disks

## Summary

Until oVirt 3.5 it was possible to copy only the disks attached to a template and only to a different storage domain. This RFE is about letting to copy also the VM and floating disks to the same or different storage domain.

## Owner

*   Name: [Tomas Jelinek](User:TJelinek)
*   Email: <tjelinek@redhat.com>

## Current status

*   Target Release: 3.6
*   Status: Done

## Proposal

*   Enable to copy the VM and floating disks
*   Enable to change the alias of the copied disk
*   Enable to copy the disk also to the same storage domain

## REST API

Send a POST request to the .../api/disks/<disk id>/copy

With

<action> <storage_domain id="14e6e9f3-9fe9-493b-b9ba-793cb441f9ad" /> <disk><alias>newDiskAlias</alias></disk> </action>

If the <disk><alias> is omitted, the same alias as the original disk will be used.

## External Resources

*   BZ: <https://bugzilla.redhat.com/show_bug.cgi?id=1132066>
*   Code: <https://gerrit.ovirt.org/#/q/status:merged+project:ovirt-engine+branch:master+topic:copyvmdisk>

[Category:oVirt 3.6 Proposed Feature](Category:oVirt 3.6 Proposed Feature) [Category:oVirt 3.6 Feature](Category:oVirt 3.6 Feature)
