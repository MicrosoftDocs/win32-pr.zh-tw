---
title: 描述項資料表總覽
description: 每個描述中繼資料表都會儲存一或多個類型的描述元-SRVs、UAVe、CBVs 和取樣器。 描述項資料表不是記憶體的配置;它只是描述項堆積中的位移和長度。
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104213"
---
# <a name="descriptor-tables-overview"></a><span data-ttu-id="93578-104">描述項資料表總覽</span><span class="sxs-lookup"><span data-stu-id="93578-104">Descriptor Tables Overview</span></span>

<span data-ttu-id="93578-105">每個描述中繼資料表都會儲存一或多個類型的描述元-SRVs、UAVe、CBVs 和取樣器。</span><span class="sxs-lookup"><span data-stu-id="93578-105">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="93578-106">描述項資料表不是記憶體的配置;它只是描述項堆積中的位移和長度。</span><span class="sxs-lookup"><span data-stu-id="93578-106">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span>

-   [<span data-ttu-id="93578-107">參考描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="93578-107">Referencing descriptor tables</span></span>](#referencing-descriptor-tables)
-   [<span data-ttu-id="93578-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="93578-108">Related topics</span></span>](#related-topics)

## <a name="referencing-descriptor-tables"></a><span data-ttu-id="93578-109">參考描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="93578-109">Referencing descriptor tables</span></span>

<span data-ttu-id="93578-110">圖形管線（透過根簽章）藉由依索引參考描述中繼資料表來取得資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="93578-110">The graphics pipeline, through the root signature, gain access to resources by referencing into descriptor tables by index.</span></span>

<span data-ttu-id="93578-111">描述項資料表實際上只是描述項堆積的子範圍。</span><span class="sxs-lookup"><span data-stu-id="93578-111">A descriptor table is actually just a sub-range of a descriptor heap.</span></span> <span data-ttu-id="93578-112">描述元堆積代表描述項集合的基礎記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="93578-112">Descriptor heaps represent the underlying memory allocation for a collection of descriptors.</span></span> <span data-ttu-id="93578-113">由於記憶體配置是建立描述項堆積的屬性，因此定義一個描述中繼資料表時，一定會比識別堆積中的區域到硬體一樣便宜。</span><span class="sxs-lookup"><span data-stu-id="93578-113">Since memory allocation is a property of a creating a descriptor heap, defining a descriptor table out of one is guaranteed to be as cheap as identifying a region in the heap to the hardware.</span></span> <span data-ttu-id="93578-114">描述中繼資料表不需要在 API 層級建立或終結，它們只會在每次參考時，將它們識別為與堆積的位移和大小。</span><span class="sxs-lookup"><span data-stu-id="93578-114">Descriptor tables don’t need to be created or destroyed at the API level– they are merely identified to drivers as an offset and size out of a heap whenever referenced.</span></span>

<span data-ttu-id="93578-115">當應用程式的著色器想要從大量可用的描述項中自由選取時，您當然可以定義非常大的描述中繼資料表， (通常會即時參考紋理)  (可能是以材質資料) 所驅動。</span><span class="sxs-lookup"><span data-stu-id="93578-115">It is certainly possible for an app to define very large descriptor tables when its shaders want the freedom to select from a vast set of available descriptors (often referencing textures) on the fly (perhaps driven by material data).</span></span>

<span data-ttu-id="93578-116">根簽章參考具有堆積參考的描述項資料表專案、資料表的開始位置 (從堆積) 開始的位移，以及資料表) 專案中 (的長度。</span><span class="sxs-lookup"><span data-stu-id="93578-116">The Root Signature references the descriptor table entry with a reference to the heap, the start location of the table (an offset from the start of the heap), and the length (in entries) of the table.</span></span> <span data-ttu-id="93578-117">下圖顯示這些概念：描述中繼資料表指標來自根簽章，以及描述項堆積內的描述元，參考上傳堆積中的完整紋理或緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="93578-117">The image below shows these concepts: the descriptor table pointers from the Root Signature and the descriptors within the descriptor heap referencing the full texture or buffer data in an upload heap.</span></span>

![描述中繼資料表](images/descriptor-table.png)

## <a name="related-topics"></a><span data-ttu-id="93578-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="93578-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93578-120">描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="93578-120">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




