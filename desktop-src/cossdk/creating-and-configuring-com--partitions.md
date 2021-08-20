---
description: 系統管理員可以使用 COM +，以程式設計方式建立和設定 COM + 分割。
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: 建立和設定 COM + 分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3cc9623272d4aba345cc666deb5c63965584af94f42dbf869b00cf7d52a2f30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858988"
---
# <a name="creating-and-configuring-com-partitions"></a>建立和設定 COM + 分割

系統管理員可以使用 COM +，以程式設計方式建立和設定 COM + 分割。 事實上，系統管理員可以從元件服務或 Active Directory 消費者和電腦系統管理工具執行的所有建立和設定工作，都可以透過使用 COM + 集合、物件和介面，或透過 Active Directory 的系統介面 (ADSI) 來完成。

**Windows XP：** 無法使用建立、設定或委派 COM + 分割的能力。 全域分割區是唯一可用的 COM + 分割。

* * Windows 2000： * * Windows 2000 中無法使用 com + 分割服務。

> [!Note]  
> 預設不會啟用 COM + 分割服務。 若要使用 COM + 分割服務，您必須透過 [元件服務] 系統管理工具啟用它，或將 [**LocalComputer**](localcomputer.md) 集合上的 PartitionsEnabled 屬性變更為 True。

 

為了完成與資料分割相關的工作，COM + 提供下列程式設計項目：

-   [**COMAdminCatalog**](comadmincatalog.md)類別上 [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)介面的方法和屬性：
    -   [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) 屬性。
    -   [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) 屬性。
    -   [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) 屬性。
    -   [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) 方法。
    -   [**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) 方法。
    -   [**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) 方法。
    -   [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) 屬性。
-   在 Active Directory 中建立和管理分割區的一組 COM + 物件。
-   用於變更磁碟分割快取大小的 COM + 登錄機碼 **PartitionCache**。
-   一組磁碟分割相關的 [Com + 系統管理集合](com--administration-collections.md)：
    -   資料 [**分割集合。**](partitions.md)
    -   [**PartitionUsers**](partitionusers.md) 集合。
    -   [**RolesForPartition**](rolesforpartition.md) 集合。
    -   [**UsersInPartitionRole**](usersinpartitionrole.md) 集合。
-   其他 [Com + 系統管理集合](com--administration-collections.md)的屬性：
    -   [**ApplicationInstances**](applicationinstances.md)集合上的 PartitionID 屬性。
    -   [**應用程式**](applications.md)集合上的 AppPartitionID 屬性。
    -   [**FilesForImport**](filesforimport.md)集合上的 PartitionDescription、PartitionID 和 PartitionName 屬性。
    -   [**LocalComputer**](localcomputer.md)集合上的 DSPartitionLookupEnabled、LocalPartitionLookupEnabled 和 PartitionsEnabled 屬性。
    -   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)集合上的 EventClassPartitionID 和 SubscriberPartitionID 屬性。
    -   [**TransientSubscriptions**](transientsubscriptions.md)集合上的 EventClassPartitionID 和 SubscriberPartitionID 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[收集分割區計量](collecting-partition-metrics.md)
</dt> <dt>

[設定資料分割快取](configuring-the-partition-cache.md)
</dt> <dt>

[將應用程式群組至資料分割](grouping-applications-into-partitions.md)
</dt> <dt>

[管理本機磁碟分割](managing-local-partitions.md)
</dt> <dt>

[管理 Active Directory 內的磁碟分割](managing-partitions-within-active-directory.md)
</dt> <dt>

[設定資料分割的系統管理許可權](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



