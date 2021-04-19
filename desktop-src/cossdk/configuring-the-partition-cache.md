---
description: COM + 分割功能包含分割區快取。 此快取會儲存使用者對分割區對應，並設計為避免重複 Active Directory 存取。
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: 設定資料分割快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973182"
---
# <a name="configuring-the-partition-cache"></a><span data-ttu-id="66bd7-104">設定資料分割快取</span><span class="sxs-lookup"><span data-stu-id="66bd7-104">Configuring the Partition Cache</span></span>

<span data-ttu-id="66bd7-105">COM + 分割功能包含分割區快取。</span><span class="sxs-lookup"><span data-stu-id="66bd7-105">The COM+ partitions feature includes a partition cache.</span></span> <span data-ttu-id="66bd7-106">此快取會儲存使用者對分割區對應，並設計為避免重複 Active Directory 存取。</span><span class="sxs-lookup"><span data-stu-id="66bd7-106">This cache stores user-to-partition mappings and is designed to avoid repetitive Active Directory access.</span></span>

## <a name="changing-cache-size"></a><span data-ttu-id="66bd7-107">變更快取大小</span><span class="sxs-lookup"><span data-stu-id="66bd7-107">Changing Cache Size</span></span>

<span data-ttu-id="66bd7-108">分割區快取是由三個數據表所組成，其大小可加以修改以增強效能。</span><span class="sxs-lookup"><span data-stu-id="66bd7-108">The partition cache consists of three tables, whose size can be modified to enhance performance.</span></span> <span data-ttu-id="66bd7-109">這些資料表包含快取中的 SID 專案數目、快取中的 OU 專案數目，以及快取中的分割區專案數目。</span><span class="sxs-lookup"><span data-stu-id="66bd7-109">These tables consist of the number of SID entries in the cache, the number of OU entries in the cache, and the number of partition entries in the cache.</span></span>

<span data-ttu-id="66bd7-110">若要變更這些資料表大小，系統管理員可以修改登錄機碼的值。</span><span class="sxs-lookup"><span data-stu-id="66bd7-110">To change these table sizes, administrators can modify the values of a registry key.</span></span> <span data-ttu-id="66bd7-111">登錄機碼和其值如下：</span><span class="sxs-lookup"><span data-stu-id="66bd7-111">The registry key and its values are as follows:</span></span>

<span data-ttu-id="66bd7-112">**HKLM \\ SOFTWARE \\ Microsoft \\ COM3 \\ PartitionCache**</span><span class="sxs-lookup"><span data-stu-id="66bd7-112">**HKLM\\SOFTWARE\\Microsoft\\COM3\\PartitionCache**</span></span>



| <span data-ttu-id="66bd7-113">金鑰值</span><span class="sxs-lookup"><span data-stu-id="66bd7-113">Key values</span></span>                         | <span data-ttu-id="66bd7-114">Description</span><span class="sxs-lookup"><span data-stu-id="66bd7-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bd7-115">**NumSidEntries**</span><span class="sxs-lookup"><span data-stu-id="66bd7-115">**NumSidEntries**</span></span><br/>       | <span data-ttu-id="66bd7-116">包含快取 \_ (預設值 = 512) 中 SID 專案數目的 REG DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="66bd7-116">Contains the REG\_DWORD value for the number of SID entries in the cache (default=512).</span></span> <span data-ttu-id="66bd7-117">此值應該設定為大於電腦將在快取失效時間範圍內服務的唯一識別數目的值。</span><span class="sxs-lookup"><span data-stu-id="66bd7-117">This value should be set to a value greater than the number of unique identities that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="66bd7-118">**NumNameEntries**</span><span class="sxs-lookup"><span data-stu-id="66bd7-118">**NumNameEntries**</span></span><br/>      | <span data-ttu-id="66bd7-119">包含快取 \_ (預設值 = 64) 中 OU 名稱專案數目的 REG DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="66bd7-119">Contains the REG\_DWORD value for the number of OU name entries in the cache (default=64).</span></span> <span data-ttu-id="66bd7-120">此值應該設定為大於電腦將在快取失效時間範圍內服務的唯一 OU 名稱數目的值。</span><span class="sxs-lookup"><span data-stu-id="66bd7-120">This value should be set to a value greater than the number of unique OU names that a machine will be servicing in the cache invalidation time window.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="66bd7-121">**NumPartitionEntries**</span><span class="sxs-lookup"><span data-stu-id="66bd7-121">**NumPartitionEntries**</span></span><br/> | <span data-ttu-id="66bd7-122">包含快取 \_ (預設值 = 1024) 中分割區專案數目的 REG DWORD 值。</span><span class="sxs-lookup"><span data-stu-id="66bd7-122">Contains the REG\_DWORD value for the number of partition entries in the cache (default=1024).</span></span><br/> <span data-ttu-id="66bd7-123">在 [快取失效時間] 視窗中，DWORD 值應該設定為大於機器所要服務之唯一分割區數目的數位。</span><span class="sxs-lookup"><span data-stu-id="66bd7-123">In the cache invalidation time window, the DWORD value should be set to a number greater than the number of unique partitions that a machine will be servicing.</span></span> <span data-ttu-id="66bd7-124">這是因為元件的內容可以包含不在該電腦上之分割區的分割區識別碼。</span><span class="sxs-lookup"><span data-stu-id="66bd7-124">This is because a component's context can include a partition ID for a partition that does not reside on that machine.</span></span> <br/> |
| <span data-ttu-id="66bd7-125">**EntryExpiration**</span><span class="sxs-lookup"><span data-stu-id="66bd7-125">**EntryExpiration**</span></span><br/>     | <span data-ttu-id="66bd7-126">包含 \_ 滴答計數的 REG DWORD 值 (每個刻度 = ~ 7 分鐘) 直到快取專案變成無效為止 (預設值 = 4 (~ 28 分鐘) ) 。</span><span class="sxs-lookup"><span data-stu-id="66bd7-126">Contains the REG\_DWORD value for the tick count (each tick = ~7 minutes) until a cache entry becomes invalid (default=4 (~28 minutes)).</span></span><br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a><span data-ttu-id="66bd7-127">清除快取</span><span class="sxs-lookup"><span data-stu-id="66bd7-127">Flushing the Cache</span></span>

<span data-ttu-id="66bd7-128">由於 COM + 會快取使用者的預設資料分割，因此您可能會想要在 Active Directory 中變更使用者的預設資料分割之後，呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="66bd7-128">Because COM+ caches the default partition for users, you might want to call this method after changing the default partition for a user in the Active Directory.</span></span> <span data-ttu-id="66bd7-129">系統管理員可以藉由呼叫 [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) 方法，以程式設計方式來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="66bd7-129">Administrators can do this programmatically by calling the [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66bd7-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="66bd7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66bd7-131">收集分割區計量</span><span class="sxs-lookup"><span data-stu-id="66bd7-131">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="66bd7-132">將應用程式群組至資料分割</span><span class="sxs-lookup"><span data-stu-id="66bd7-132">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="66bd7-133">管理本機磁碟分割</span><span class="sxs-lookup"><span data-stu-id="66bd7-133">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="66bd7-134">管理 Active Directory 內的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="66bd7-134">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="66bd7-135">設定資料分割的系統管理許可權</span><span class="sxs-lookup"><span data-stu-id="66bd7-135">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




