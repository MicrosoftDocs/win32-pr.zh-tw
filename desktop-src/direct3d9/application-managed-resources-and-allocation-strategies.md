---
description: Managed 頂點緩衝區或索引緩衝區資源無法在建立時指定 D3DUSAGE 動態宣告為動態 \_ 。
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed (Direct3D 9) 的資源和配置策略
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991627"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a><span data-ttu-id="5a284-103">Application-Managed (Direct3D 9) 的資源和配置策略</span><span class="sxs-lookup"><span data-stu-id="5a284-103">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>

<span data-ttu-id="5a284-104">Managed 頂點緩衝區或索引緩衝區資源無法在建立時指定 D3DUSAGE 動態宣告為動態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5a284-104">Managed vertex-buffer or index-buffer resources cannot be declared dynamic by specifying D3DUSAGE\_DYNAMIC at creation time.</span></span> <span data-ttu-id="5a284-105">這需要針對頂點緩衝區內容的每次修改進行額外的複製。</span><span class="sxs-lookup"><span data-stu-id="5a284-105">This would require an additional copy for every modification to the vertex buffer contents.</span></span> <span data-ttu-id="5a284-106">動態頂點緩衝區適用于轉譯動態幾何，以及從二進位空間分割樹狀結構或其他可視性資料結構提取的資料。</span><span class="sxs-lookup"><span data-stu-id="5a284-106">Dynamic vertex buffers are intended for rendering dynamic geometry and data pulled in from binary space partitioned trees or other visibility data structures.</span></span> <span data-ttu-id="5a284-107">這可以透過預先配置所需格式的緩衝區來完成。</span><span class="sxs-lookup"><span data-stu-id="5a284-107">This can be accomplished by pre-allocating buffers of the desired format.</span></span> <span data-ttu-id="5a284-108">然後 parceled 這些資源，以支援應用程式內的資源管理員所需的應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="5a284-108">These resources are then parceled out to support application needs by a resource manager within the application.</span></span> <span data-ttu-id="5a284-109">動態頂點緩衝區總數很小，因為應用程式只會使用幾個不同的頂點進展，而且因為唯一的進展需要不同的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5a284-109">The total number of dynamic vertex buffers is small because an application will use simultaneously only a few different vertex strides and because a different vertex buffer is required only for unique strides.</span></span> <span data-ttu-id="5a284-110">以這種方式管理動態資源時，請確定對資源的高頻率需求不會大幅降低應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="5a284-110">When managing dynamic resources in this way, ensure that high-frequency demands on the resources do not significantly decrease the application's performance.</span></span>

<span data-ttu-id="5a284-111">使用 Direct3D 和應用程式所管理的資源時，請在 \_ 建立 direct3d 管理的資源之前，先在 D3DPOOL 預設記憶體中配置應用程式管理的資源。</span><span class="sxs-lookup"><span data-stu-id="5a284-111">When using resources managed by both Direct3D and applications, allocate application-managed resources in D3DPOOL\_DEFAULT memory prior to creating Direct3D-managed resources.</span></span> <span data-ttu-id="5a284-112">這可讓記憶體管理員維持準確的可用記憶體計數。</span><span class="sxs-lookup"><span data-stu-id="5a284-112">This enables the memory manager to maintain an accurate count of available memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a284-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a284-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a284-114">Direct3D 資源</span><span class="sxs-lookup"><span data-stu-id="5a284-114">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



