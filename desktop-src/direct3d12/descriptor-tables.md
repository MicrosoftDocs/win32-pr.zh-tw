---
title: 描述中繼資料表
description: 描述項資料表在邏輯上是描述項的陣列。
ms.assetid: 5faf294f-acd5-4b39-92f4-1d6b2abe3040
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10414f8458006029f3279203e949b43410911fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103692"
---
# <a name="descriptor-tables"></a><span data-ttu-id="02fd7-103">描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="02fd7-103">Descriptor Tables</span></span>

<span data-ttu-id="02fd7-104">描述項資料表在邏輯上是描述項的陣列。</span><span class="sxs-lookup"><span data-stu-id="02fd7-104">A descriptor table is logically an array of descriptors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="02fd7-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="02fd7-105">In this section</span></span>



| <span data-ttu-id="02fd7-106">主題</span><span class="sxs-lookup"><span data-stu-id="02fd7-106">Topic</span></span>                                                                                 | <span data-ttu-id="02fd7-107">描述</span><span class="sxs-lookup"><span data-stu-id="02fd7-107">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02fd7-108">描述項資料表總覽</span><span class="sxs-lookup"><span data-stu-id="02fd7-108">Descriptor Tables Overview</span></span>](descriptor-tables-overview.md)<br/>               | <span data-ttu-id="02fd7-109">每個描述中繼資料表都會儲存一或多個類型的描述元-SRVs、UAVe、CBVs 和取樣器。</span><span class="sxs-lookup"><span data-stu-id="02fd7-109">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="02fd7-110">描述項資料表不是記憶體的配置;它只是描述項堆積中的位移和長度。</span><span class="sxs-lookup"><span data-stu-id="02fd7-110">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span><br/> |
| [<span data-ttu-id="02fd7-111">使用描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="02fd7-111">Using Descriptor Tables</span></span>](using-descriptor-tables.md)<br/>                     | <span data-ttu-id="02fd7-112">描述項資料表中，每個都識別描述元堆積中的範圍，都會系結至命令清單上目前的根簽章所定義的位置。</span><span class="sxs-lookup"><span data-stu-id="02fd7-112">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span> <br/>                                                               |
| [<span data-ttu-id="02fd7-113">描述項資料表的 Advanced 使用</span><span class="sxs-lookup"><span data-stu-id="02fd7-113">Advanced Use of Descriptor Tables</span></span>](advanced-use-of-descriptor-tables.md)<br/> | <span data-ttu-id="02fd7-114">下列各節提供有關描述項資料表的 advanced 使用資訊。</span><span class="sxs-lookup"><span data-stu-id="02fd7-114">The following sections provide information about the advanced use of descriptor tables.</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="02fd7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="02fd7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02fd7-116">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="02fd7-116">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="02fd7-117">資源系結</span><span class="sxs-lookup"><span data-stu-id="02fd7-117">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="02fd7-118">根簽章</span><span class="sxs-lookup"><span data-stu-id="02fd7-118">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





