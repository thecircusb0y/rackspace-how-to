---
permalink: rackspace-cloud-backup-vs-cloud-server-image-backups/
node_id: 1427
title: Rackspace Cloud Backup vs. Cloud Server Image Backups
type: article
created_date: '2012-06-06'
created_by: Rackspace Support
last_modified_date: '2015-12-31'
last_modified_by: Stephanie Fillmon
product: Cloud Backup
product_url: cloud-backup
---

Some users are used to taking snapshots of their [Cloud Servers](http://www.rackspace.com/cloud/servers) 
as a backup. If you require a solution that saves the server's state or configuration,
or you want to keep gold copies of your system, then you can create an image
backup of the server. The backup saves the whole server in 
a single file that you can use to 
easily recreate a new server with an identical configuration and
state. However, an image backup does not 
give you any control over the individual files on the server. For example, you cannot 
use the image to recover or update a single file. 

**Note:** You can learn more about scheduling images from the [Scheduled
Images
FAQ](/how-to/scheduled-images-faq).

Rackspace Cloud Backup, on the other hand, is a **FILE-BASED backup**.
that allows you to specify what folders or files to backup or
restore. You can still use Cloud Backup to backup or restore the whole system
with all its folders, but the distinction with image backups is that the
granularity of Rackspace Cloud Backup is at the file level, as opposed
to it being at the whole server image level.

Moreover, Rackspace Cloud Backup is also an **INCREMENTAL backup** tool
in that it only copies the portion of the files that changed for those
files that actually changed. This gives you some flexibility because,
with the exception of your first complete backup, every subsequent
backup is just a "delta" of the previous backup, which makes for faster
backup and restores operations and also reduces the storage required. As
you probably know, image backups are not incremental: they copy the
whole system every time.

Rackspace customers now have two options for backing up their Cloud
Servers. Below is a summary of both:

-   **Rackspace Cloud Backup** - Rackspace Cloud Backup is a fully
    integrated, file-based backup solution that helps protect your data
    on cloud servers. For additional information, check out our
    Cloud Backup Overview](/how-to/rackspace-cloud-backup-overview).

<!-- -->

-   **Cloud Server Image Backup** - Cloud Server Image Backup is a copy
    of the entire state of a Cloud Server stored either on Cloud Files
    or on the Cloud Server's host, depending on the environment. Images
    can be scheduled or created on-demand. For additional information,
    check out [Creating A New Cloud Server
    From A Saved
    Image](/how-to/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image)

**NOTE:** With General Purpose and I/O-optimized Cloud Servers, only the
system disk is captured when using an Image Backup. If you require
backups of your data disk or disks, use Cloud Backup so you can configure
your backup to include the specific drives and directories you want to
retain. To determine which product best suits your backup needs, visit
the links below:

-   **[Cloud Block Storage
    overview](/how-to/cloud-block-storage-overview)**
-   **[Best practices for backing up your data: Cloud Block Storage
    versus Cloud
    Backup](/how-to/best-practices-for-backing-up-your-data-cloud-block-storage-versus-cloud-backup)**
