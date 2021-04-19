---
description: 將應用程式群組至資料分割
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: 將應用程式群組至資料分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973594"
---
# <a name="grouping-applications-into-partitions"></a><span data-ttu-id="d8363-103">將應用程式群組至資料分割</span><span class="sxs-lookup"><span data-stu-id="d8363-103">Grouping Applications into Partitions</span></span>

<span data-ttu-id="d8363-104">當您決定如何將應用程式群組至資料分割時，系統管理員必須留意特定的規則和限制，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="d8363-104">When deciding how to group applications into partitions, administrators need to be aware of certain rules and restrictions, including the following:</span></span>

-   <span data-ttu-id="d8363-105">您可以將應用程式安裝到一或多個磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="d8363-105">An application can be installed into one or more partitions.</span></span>
-   <span data-ttu-id="d8363-106">應用程式中只能存在一個指定元件的實例。</span><span class="sxs-lookup"><span data-stu-id="d8363-106">Only one instance of a given component can exist in an application.</span></span>

## <a name="public-and-private-components"></a><span data-ttu-id="d8363-107">公用和私用元件</span><span class="sxs-lookup"><span data-stu-id="d8363-107">Public and Private Components</span></span>

<span data-ttu-id="d8363-108">決定如何分組 COM + 應用程式時，會有其他限制。</span><span class="sxs-lookup"><span data-stu-id="d8363-108">Other restrictions exist when deciding how to group COM+ applications.</span></span> <span data-ttu-id="d8363-109">這些限制與應用程式內的公用或私用元件相關。</span><span class="sxs-lookup"><span data-stu-id="d8363-109">These restrictions pertain to public versus private components within an application.</span></span> <span data-ttu-id="d8363-110">應用程式元件通常可以是公用或私用。</span><span class="sxs-lookup"><span data-stu-id="d8363-110">Application components can generally be either public or private.</span></span> <span data-ttu-id="d8363-111">不過，將應用程式群組成分割區時，系統管理員應留意公用和私用元件的一些限制。</span><span class="sxs-lookup"><span data-stu-id="d8363-111">However, when grouping applications into partitions, administrators should be aware of some restrictions around public and private components.</span></span> <span data-ttu-id="d8363-112">下表列出這些限制。</span><span class="sxs-lookup"><span data-stu-id="d8363-112">The following table lists these restrictions.</span></span>



| <span data-ttu-id="d8363-113">如果應用程式為：</span><span class="sxs-lookup"><span data-stu-id="d8363-113">If an application is:</span></span>              | <span data-ttu-id="d8363-114">然後，磁碟分割中的元件可以是：</span><span class="sxs-lookup"><span data-stu-id="d8363-114">Then components in a partition can be:</span></span>                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8363-115">伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="d8363-115">A server application</span></span><br/>    | <span data-ttu-id="d8363-116">公用和私用。</span><span class="sxs-lookup"><span data-stu-id="d8363-116">Public and private.</span></span><br/>                                                                                           |
| <span data-ttu-id="d8363-117">程式庫應用程式</span><span class="sxs-lookup"><span data-stu-id="d8363-117">A library application</span></span><br/>   | <span data-ttu-id="d8363-118">僅限 Public。</span><span class="sxs-lookup"><span data-stu-id="d8363-118">Public only.</span></span> <span data-ttu-id="d8363-119">否則，呼叫端應用程式可能會有相同的元件，而這會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="d8363-119">Otherwise, the callers application could have the same components, which would create ambiguity.</span></span><br/> |
| <span data-ttu-id="d8363-120">在全域資料分割中</span><span class="sxs-lookup"><span data-stu-id="d8363-120">In the global partition</span></span><br/> | <span data-ttu-id="d8363-121">僅限 Public。</span><span class="sxs-lookup"><span data-stu-id="d8363-121">Public only.</span></span> <span data-ttu-id="d8363-122">這可確保回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="d8363-122">This ensures backward compatibility.</span></span><br/>                                                             |



 

## <a name="application-ids"></a><span data-ttu-id="d8363-123">應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="d8363-123">Application IDs</span></span>

<span data-ttu-id="d8363-124">每個安裝在電腦上的 COM + 應用程式都有唯一的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8363-124">Every COM+ application installed on a computer has a unique application ID.</span></span> <span data-ttu-id="d8363-125">不過，應用程式名稱只需要在單一磁碟分割中，而不是整部電腦上的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d8363-125">However, application names need only be unique within a single partition and not on the entire computer.</span></span>

<span data-ttu-id="d8363-126">下表顯示當應用程式匯入分割區或從分割區匯出時，應用程式識別碼會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="d8363-126">The following table shows what happens to the application ID when an application is imported into a partition or exported from a partition.</span></span>



| <span data-ttu-id="d8363-127">如果應用程式為：</span><span class="sxs-lookup"><span data-stu-id="d8363-127">If an application is:</span></span>                                              | <span data-ttu-id="d8363-128">然後是應用程式識別碼：</span><span class="sxs-lookup"><span data-stu-id="d8363-128">Then the application ID:</span></span>                    |
|--------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="d8363-129">匯入至全域分割區</span><span class="sxs-lookup"><span data-stu-id="d8363-129">Imported to the global partition</span></span><br/>                        | <span data-ttu-id="d8363-130">保持不變</span><span class="sxs-lookup"><span data-stu-id="d8363-130">Remains the same</span></span><br/>                 |
| <span data-ttu-id="d8363-131">匯入至全域資料分割以外的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="d8363-131">Imported to a partition other than the global partition</span></span><br/> | <span data-ttu-id="d8363-132">已變更</span><span class="sxs-lookup"><span data-stu-id="d8363-132">Is changed</span></span><br/>                       |
| <span data-ttu-id="d8363-133">已匯出</span><span class="sxs-lookup"><span data-stu-id="d8363-133">Exported</span></span><br/>                                                | <span data-ttu-id="d8363-134">包含在匯出的檔案中</span><span class="sxs-lookup"><span data-stu-id="d8363-134">Is included in the exported file</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="d8363-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8363-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8363-136">收集分割區計量</span><span class="sxs-lookup"><span data-stu-id="d8363-136">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="d8363-137">設定資料分割快取</span><span class="sxs-lookup"><span data-stu-id="d8363-137">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="d8363-138">管理本機磁碟分割</span><span class="sxs-lookup"><span data-stu-id="d8363-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="d8363-139">管理 Active Directory 內的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="d8363-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="d8363-140">設定資料分割的系統管理許可權</span><span class="sxs-lookup"><span data-stu-id="d8363-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




