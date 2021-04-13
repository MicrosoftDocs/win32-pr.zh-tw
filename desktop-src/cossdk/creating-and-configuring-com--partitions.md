---
description: 系統管理員可以使用 COM +，以程式設計方式建立和設定 COM + 分割。
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: 建立和設定 COM + 分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510551"
---
# <a name="creating-and-configuring-com-partitions"></a><span data-ttu-id="acdd0-103">建立和設定 COM + 分割</span><span class="sxs-lookup"><span data-stu-id="acdd0-103">Creating and Configuring COM+ Partitions</span></span>

<span data-ttu-id="acdd0-104">系統管理員可以使用 COM +，以程式設計方式建立和設定 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="acdd0-104">Administrators can use COM+ to programmatically create and configure COM+ partitions.</span></span> <span data-ttu-id="acdd0-105">事實上，系統管理員可以從元件服務或 Active Directory 消費者和電腦系統管理工具執行的所有建立和設定工作，都可以透過使用 COM + 集合、物件和介面，或透過 Active Directory 的系統介面 (ADSI) 來完成。</span><span class="sxs-lookup"><span data-stu-id="acdd0-105">In fact, all creation and configuration tasks that an administrator can do from the Component Services or the Active Directory Users and Computers administrative tools can be done by using COM+ collections, objects, and interfaces or through the Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="acdd0-106">**WINDOWS XP：** 無法使用建立、設定或委派 COM + 分割的能力。</span><span class="sxs-lookup"><span data-stu-id="acdd0-106">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="acdd0-107">全域分割區是唯一可用的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="acdd0-107">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="acdd0-108">\* \* Windows 2000： \* \* COM + 分割服務無法在 Windows 2000 中使用。</span><span class="sxs-lookup"><span data-stu-id="acdd0-108">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

> [!Note]  
> <span data-ttu-id="acdd0-109">預設不會啟用 COM + 分割服務。</span><span class="sxs-lookup"><span data-stu-id="acdd0-109">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="acdd0-110">若要使用 COM + 分割服務，您必須透過 [元件服務] 系統管理工具啟用它，或將 [**LocalComputer**](localcomputer.md) 集合上的 PartitionsEnabled 屬性變更為 True。</span><span class="sxs-lookup"><span data-stu-id="acdd0-110">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="acdd0-111">為了完成與資料分割相關的工作，COM + 提供下列程式設計項目：</span><span class="sxs-lookup"><span data-stu-id="acdd0-111">To accomplish partition-related tasks, COM+ provides the following programming elements:</span></span>

-   <span data-ttu-id="acdd0-112">[**COMAdminCatalog**](comadmincatalog.md)類別上 [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)介面的方法和屬性：</span><span class="sxs-lookup"><span data-stu-id="acdd0-112">Methods and properties of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface on the [**COMAdminCatalog**](comadmincatalog.md) class:</span></span>
    -   <span data-ttu-id="acdd0-113">[**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-113">[**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) property.</span></span>
    -   <span data-ttu-id="acdd0-114">[**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-114">[**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) property.</span></span>
    -   <span data-ttu-id="acdd0-115">[**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-115">[**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) property.</span></span>
    -   <span data-ttu-id="acdd0-116">[**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) 方法。</span><span class="sxs-lookup"><span data-stu-id="acdd0-116">[**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>
    -   <span data-ttu-id="acdd0-117">[**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) 方法。</span><span class="sxs-lookup"><span data-stu-id="acdd0-117">[**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) method.</span></span>
    -   <span data-ttu-id="acdd0-118">[**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) 方法。</span><span class="sxs-lookup"><span data-stu-id="acdd0-118">[**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) method.</span></span>
    -   <span data-ttu-id="acdd0-119">[**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-119">[**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) property.</span></span>
-   <span data-ttu-id="acdd0-120">在 Active Directory 中建立和管理分割區的一組 COM + 物件。</span><span class="sxs-lookup"><span data-stu-id="acdd0-120">A set of COM+ objects for creating and managing partitions in Active Directory.</span></span>
-   <span data-ttu-id="acdd0-121">用於變更磁碟分割快取大小的 COM + 登錄機碼 **PartitionCache**。</span><span class="sxs-lookup"><span data-stu-id="acdd0-121">A COM+ registry key, **PartitionCache**, for changing the partition cache size.</span></span>
-   <span data-ttu-id="acdd0-122">一組磁碟分割相關的 [Com + 系統管理集合](com--administration-collections.md)：</span><span class="sxs-lookup"><span data-stu-id="acdd0-122">A set of partitions-related [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="acdd0-123">資料 [**分割集合。**](partitions.md)</span><span class="sxs-lookup"><span data-stu-id="acdd0-123">[**Partitions**](partitions.md) collection.</span></span>
    -   <span data-ttu-id="acdd0-124">[**PartitionUsers**](partitionusers.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="acdd0-124">[**PartitionUsers**](partitionusers.md) collection.</span></span>
    -   <span data-ttu-id="acdd0-125">[**RolesForPartition**](rolesforpartition.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="acdd0-125">[**RolesForPartition**](rolesforpartition.md) collection.</span></span>
    -   <span data-ttu-id="acdd0-126">[**UsersInPartitionRole**](usersinpartitionrole.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="acdd0-126">[**UsersInPartitionRole**](usersinpartitionrole.md) collection.</span></span>
-   <span data-ttu-id="acdd0-127">其他 [Com + 系統管理集合](com--administration-collections.md)的屬性：</span><span class="sxs-lookup"><span data-stu-id="acdd0-127">Properties of other [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="acdd0-128">[**ApplicationInstances**](applicationinstances.md)集合上的 PartitionID 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-128">PartitionID property on the [**ApplicationInstances**](applicationinstances.md) collection.</span></span>
    -   <span data-ttu-id="acdd0-129">[**應用程式**](applications.md)集合上的 AppPartitionID 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-129">AppPartitionID property on the [**Applications**](applications.md) collection.</span></span>
    -   <span data-ttu-id="acdd0-130">[**FilesForImport**](filesforimport.md)集合上的 PartitionDescription、PartitionID 和 PartitionName 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-130">PartitionDescription, PartitionID, and PartitionName properties on the [**FilesForImport**](filesforimport.md) collection.</span></span>
    -   <span data-ttu-id="acdd0-131">[**LocalComputer**](localcomputer.md)集合上的 DSPartitionLookupEnabled、LocalPartitionLookupEnabled 和 PartitionsEnabled 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-131">DSPartitionLookupEnabled, LocalPartitionLookupEnabled, and PartitionsEnabled properties on the [**LocalComputer**](localcomputer.md) collection.</span></span>
    -   <span data-ttu-id="acdd0-132">[**SubscriptionsForComponent**](subscriptionsforcomponent.md)集合上的 EventClassPartitionID 和 SubscriberPartitionID 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-132">EventClassPartitionID and SubscriberPartitionID properties on the [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>
    -   <span data-ttu-id="acdd0-133">[**TransientSubscriptions**](transientsubscriptions.md)集合上的 EventClassPartitionID 和 SubscriberPartitionID 屬性。</span><span class="sxs-lookup"><span data-stu-id="acdd0-133">EventClassPartitionID and SubscriberPartitionID properties on the [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acdd0-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="acdd0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acdd0-135">收集分割區計量</span><span class="sxs-lookup"><span data-stu-id="acdd0-135">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="acdd0-136">設定資料分割快取</span><span class="sxs-lookup"><span data-stu-id="acdd0-136">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="acdd0-137">將應用程式群組至資料分割</span><span class="sxs-lookup"><span data-stu-id="acdd0-137">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="acdd0-138">管理本機磁碟分割</span><span class="sxs-lookup"><span data-stu-id="acdd0-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="acdd0-139">管理 Active Directory 內的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="acdd0-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="acdd0-140">設定資料分割的系統管理許可權</span><span class="sxs-lookup"><span data-stu-id="acdd0-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



