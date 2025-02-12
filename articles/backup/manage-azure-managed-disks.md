---
title: Manage Azure Managed Disks
description: Learn about managing Azure Managed Disk from the Azure portal.
ms.topic: conceptual
ms.date: 09/06/2021
---

# Manage Azure Managed Disks

This article explains how to manage Azure Managed Disk from the Azure portal.

## Stop Protection (Preview)


There are three ways by which you can stop protecting an Azure Disk:

- **Stop Protection and Retain Data (Retain forever)**: This option helps you stop all future backup jobs from protecting your disk. However, Azure Backup service will retain the recovery points that are backed up forever. You'll need to pay to keep the recovery points in the vault (see [Azure Backup pricing](https://azure.microsoft.com/pricing/details/backup/) for details). You'll be able to restore the disk, if needed. To resume disk protection, use the **Resume backup** option.

- **Stop Protection and Retain Data (Retain as per Policy)**: This option helps you stop all future backup jobs from protecting your disk. The recovery points will be retained as per policy and will be chargeable according to [Azure Backup pricing](https://azure.microsoft.com/pricing/details/backup/). However, the latest recovery point will be retained forever.

- **Stop Protection and Delete Data**: This option helps you stop all future backup jobs from protecting your disks and delete all the recovery points. You won't be able to restore the disk or use the **Resume backup** option.

### Stop Protection and Retain Data

1. Go to **Backup center** and select **Azure Disks**.

1. From the list of disk backup instances, select the instance that you want to retain.

1. Select **Stop Backup (Preview)**.

   :::image type="content" source="./media/manage-azure-managed-disks/select-disk-backup-instance-to-stop-inline.png" alt-text="Screenshot showing the selection of the Azure disk backup instance to be stopped." lightbox="./media/manage-azure-managed-disks/select-disk-backup-instance-to-stop-expanded.png":::
 
1. Select one of the following data retention options:

   1. Retain forever
   1. Retain as per policy
 
   :::image type="content" source="./media/manage-azure-managed-disks/data-retention-options-for-disk-inline.png" alt-text="Screenshot showing the options to stop disk backup instance protection." lightbox="./media/manage-azure-managed-disks/data-retention-options-for-disk-expanded.png":::

   You can also select the reason for stopping backups  from the drop-down list.

1. Click **Stop Backup**.

1. Select **Confirm** to stop data protection.

   :::image type="content" source="./media/manage-azure-managed-disks/confirm-stopping-disk-backup-inline.png" alt-text="Screenshot showing the options for disk backup instance retention to be selected." lightbox="./media/manage-azure-managed-disks/confirm-stopping-disk-backup-expanded.png":::

### Stop Protection and Delete Data

1. Go to **Backup center** and select **Azure Disks**.

1. From the list of disk backup instances, select the instance that you want to delete.

1. Click **Stop Backup (Preview)**.

1. Select **Delete Backup Data**.

   Provide the name of the backup instance, reason for deletion, and any other comments.

   :::image type="content" source="./media/manage-azure-managed-disks/details-to-stop-disk-backup-inline.png" alt-text="Screenshot for the confirmation for stopping disk backup." lightbox="./media/manage-azure-managed-disks/details-to-stop-disk-backup-expanded.png":::

1. Select **Stop Backup**.

1. Select **Confirm** to stop data protection.

   :::image type="content" source="./media/manage-azure-managed-disks/confirm-stopping-disk-backup-inline.png" alt-text="Screenshot showing the options for disk backup instance retention to be selected." lightbox="./media/manage-azure-managed-disks/confirm-stopping-disk-backup-expanded.png":::

## Resume Protection

If you have selected the **Stop Protection and Retain data** option, you can resume protection for your disks.

Use the following steps:

1. Go to **Backup center** and select **Azure Disks**.

1. From the list of disk backup instances, select the instance that you want to resume.

1. Select **Resume Backup (Preview)**.

   :::image type="content" source="./media/manage-azure-managed-disks/resume-disk-protection-inline.png" alt-text="Screenshot showing the option to resume protection of disk." lightbox="./media/manage-azure-managed-disks/resume-disk-protection-expanded.png":::

1. Select **Resume backup**.

   :::image type="content" source="./media/manage-azure-managed-disks/resume-disk-backup-inline.png" alt-text="Screenshot showing the option to resume disk backup." lightbox="./media/manage-azure-managed-disks/resume-disk-backup-expanded.png":::


## Next steps

[Backup vaults overview](backup-vault-overview.md)
