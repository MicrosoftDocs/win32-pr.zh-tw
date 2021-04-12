---
description: COM + 分割工作
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: COM + 分割工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187660"
---
# <a name="com-partitions-tasks"></a><span data-ttu-id="da68f-103">COM + 分割工作</span><span class="sxs-lookup"><span data-stu-id="da68f-103">COM+ Partitions Tasks</span></span>

<span data-ttu-id="da68f-104">本節中的下列主題提供使用 COM + 磁碟分割的逐步指示。</span><span class="sxs-lookup"><span data-stu-id="da68f-104">The following topics in this section provide step-by-step instructions for using COM+ partitions.</span></span>

<span data-ttu-id="da68f-105">**WINDOWS XP：** 無法使用建立、設定或委派 COM + 分割的能力。</span><span class="sxs-lookup"><span data-stu-id="da68f-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="da68f-106">全域分割區是唯一可用的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="da68f-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="da68f-107">\* \* Windows 2000： \* \* COM + 分割服務無法在 Windows 2000 中使用。</span><span class="sxs-lookup"><span data-stu-id="da68f-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>



| <span data-ttu-id="da68f-108">主題</span><span class="sxs-lookup"><span data-stu-id="da68f-108">Topic</span></span>                                                                                                         | <span data-ttu-id="da68f-109">描述</span><span class="sxs-lookup"><span data-stu-id="da68f-109">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da68f-110">建立和設定 COM + 分割</span><span class="sxs-lookup"><span data-stu-id="da68f-110">Creating and Configuring COM+ Partitions</span></span>](creating-and-configuring-com--partitions.md)<br/>           | <span data-ttu-id="da68f-111">描述如何建立和設定 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="da68f-111">Describes how to create and configure a COM+ partition.</span></span><br/>                             |
| [<span data-ttu-id="da68f-112">管理本機磁碟分割</span><span class="sxs-lookup"><span data-stu-id="da68f-112">Managing Local Partitions</span></span>](managing-local-partitions.md)<br/>                                         | <span data-ttu-id="da68f-113">描述如何管理不在 Active Directory 內的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="da68f-113">Describes how to manage COM+ partitions that are not within Active Directory.</span></span><br/>       |
| [<span data-ttu-id="da68f-114">管理 Active Directory 內的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="da68f-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)<br/>     | <span data-ttu-id="da68f-115">描述如何管理 Active Directory 內指定的 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="da68f-115">Describes how to manage COM+ partitions that are specified within Active Directory.</span></span><br/> |
| [<span data-ttu-id="da68f-116">設定資料分割的系統管理許可權</span><span class="sxs-lookup"><span data-stu-id="da68f-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)<br/> | <span data-ttu-id="da68f-117">描述如何設定 COM + 磁碟分割的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="da68f-117">Describes how to set security privileges for a COM+ partition.</span></span><br/>                      |
| [<span data-ttu-id="da68f-118">將應用程式群組至資料分割</span><span class="sxs-lookup"><span data-stu-id="da68f-118">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)<br/>                 | <span data-ttu-id="da68f-119">描述如何將 COM + 應用程式設定為屬於 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="da68f-119">Describes how to configure COM+ applications to belong to a COM+ partition.</span></span> <br/>        |
| [<span data-ttu-id="da68f-120">收集分割區計量</span><span class="sxs-lookup"><span data-stu-id="da68f-120">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)<br/>                                   | <span data-ttu-id="da68f-121">說明如何收集 COM + 分割的相關資料。</span><span class="sxs-lookup"><span data-stu-id="da68f-121">Describes how to collect data about COM+ partitions.</span></span><br/>                                |
| [<span data-ttu-id="da68f-122">設定資料分割快取</span><span class="sxs-lookup"><span data-stu-id="da68f-122">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)<br/>                             | <span data-ttu-id="da68f-123">描述如何設定 COM + 分割區快取。</span><span class="sxs-lookup"><span data-stu-id="da68f-123">Describes how to configure the COM+ partition cache.</span></span><br/>                                |



 

> [!Note]  
> <span data-ttu-id="da68f-124">預設不會啟用 COM + 分割服務。</span><span class="sxs-lookup"><span data-stu-id="da68f-124">The COM+ Partitions service is not enabled by default.</span></span> <span data-ttu-id="da68f-125">若要使用 COM + 分割服務，您必須透過 [元件服務] 系統管理工具啟用它，或將 [**LocalComputer**](localcomputer.md) 集合上的 PartitionsEnabled 屬性變更為 True。</span><span class="sxs-lookup"><span data-stu-id="da68f-125">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da68f-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="da68f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da68f-127">COM + 磁碟分割概念</span><span class="sxs-lookup"><span data-stu-id="da68f-127">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)
</dt> </dl>

 

 




