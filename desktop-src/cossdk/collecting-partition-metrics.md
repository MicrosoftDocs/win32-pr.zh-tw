---
description: 收集分割區計量
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: 收集分割區計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110409"
---
# <a name="collecting-partition-metrics"></a><span data-ttu-id="7b3d5-103">收集分割區計量</span><span class="sxs-lookup"><span data-stu-id="7b3d5-103">Collecting Partition Metrics</span></span>

<span data-ttu-id="7b3d5-104">在某些情況下，組織可能會想要針對監視、容量規劃和資源計量的用途，收集 COM + 應用程式使用的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7b3d5-104">In some cases, an organization might want to collect information on COM+ application use for the purposes of monitoring, capacity planning, and resource accounting.</span></span>

<span data-ttu-id="7b3d5-105">例如，應用程式服務提供者 (ASP) 可能會想要對客戶收取其資源使用量的費用。</span><span class="sxs-lookup"><span data-stu-id="7b3d5-105">For example, an application service provider (ASP) might want to charge a customer for its resource usage.</span></span> <span data-ttu-id="7b3d5-106">若要這樣做，COM + 可讓您根據每個資料分割收集事件和計量資訊。</span><span class="sxs-lookup"><span data-stu-id="7b3d5-106">To do this, COM+ allows you to collect event and metrics information on a per-partition basis.</span></span>

<span data-ttu-id="7b3d5-107">針對特定資料分割收集這項資訊的方式，就是針對每個 COM + 檢測介面，指定標準事件結構內的資料分割識別碼成員。</span><span class="sxs-lookup"><span data-stu-id="7b3d5-107">The way to collect this information for a specific partition is by specifying, for each COM+ instrumentation interface, the partition ID member within the standard event structure.</span></span> <span data-ttu-id="7b3d5-108">事件結構是 COM + 檢測介面的第一個值。</span><span class="sxs-lookup"><span data-stu-id="7b3d5-108">The event structure is the first value of a COM+ instrumentation interface.</span></span> <span data-ttu-id="7b3d5-109">如需詳細資訊，請參閱 [Com + 檢測介面](com--instrumentation-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7b3d5-109">For more information, see [COM+ Instrumentation Interfaces](com--instrumentation-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b3d5-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b3d5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b3d5-111">設定資料分割快取</span><span class="sxs-lookup"><span data-stu-id="7b3d5-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="7b3d5-112">將應用程式群組至資料分割</span><span class="sxs-lookup"><span data-stu-id="7b3d5-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="7b3d5-113">管理本機磁碟分割</span><span class="sxs-lookup"><span data-stu-id="7b3d5-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="7b3d5-114">管理 Active Directory 內的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="7b3d5-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="7b3d5-115">設定資料分割的系統管理許可權</span><span class="sxs-lookup"><span data-stu-id="7b3d5-115">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



