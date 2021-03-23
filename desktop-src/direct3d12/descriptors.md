---
title: 描述項
description: 描述項是 D3D12 中單一資源的系結主要單位。
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104692"
---
# <a name="descriptors"></a><span data-ttu-id="99f8e-103">描述項</span><span class="sxs-lookup"><span data-stu-id="99f8e-103">Descriptors</span></span>

<span data-ttu-id="99f8e-104">描述項是 D3D12 中單一資源的系結主要單位。</span><span class="sxs-lookup"><span data-stu-id="99f8e-104">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99f8e-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="99f8e-105">In this section</span></span>



| <span data-ttu-id="99f8e-106">主題</span><span class="sxs-lookup"><span data-stu-id="99f8e-106">Topic</span></span>                                                       | <span data-ttu-id="99f8e-107">描述</span><span class="sxs-lookup"><span data-stu-id="99f8e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99f8e-108">描述項總覽</span><span class="sxs-lookup"><span data-stu-id="99f8e-108">Descriptors Overview</span></span>](descriptors-overview.md)<br/> | <span data-ttu-id="99f8e-109">描述元是由 API 呼叫所建立，並識別資源。</span><span class="sxs-lookup"><span data-stu-id="99f8e-109">Descriptors are created by API calls and identify resources.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="99f8e-110">建立描述項</span><span class="sxs-lookup"><span data-stu-id="99f8e-110">Creating Descriptors</span></span>](creating-descriptors.md)<br/> | <span data-ttu-id="99f8e-111">描述並顯示建立索引、頂點和常數緩衝區視圖的範例;著色器資源、轉譯目標、未排序的存取、資料流程輸出和深度樣板視圖;和取樣器。</span><span class="sxs-lookup"><span data-stu-id="99f8e-111">Describes and shows examples for creating index, vertex, and constant buffer views; shader resource, render target, unordered access, stream output and depth-stencil views; and samplers.</span></span> <span data-ttu-id="99f8e-112">建立描述項的所有方法都是無限制執行緒。</span><span class="sxs-lookup"><span data-stu-id="99f8e-112">All methods for creating descriptors are free threaded.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="99f8e-113">複製描述項</span><span class="sxs-lookup"><span data-stu-id="99f8e-113">Copying Descriptors</span></span>](copying-descriptors.md)<br/>   | <span data-ttu-id="99f8e-114">裝置介面上的 [**ID3D12Device：： CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) 和 [**ID3D12Device：： CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) 方法會使用 CPU 來立即複製描述項。</span><span class="sxs-lookup"><span data-stu-id="99f8e-114">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="99f8e-115">只要 CPU 或 GPU 上的多個執行緒不會執行任何可能衝突的寫入，就可以將它們稱為「自由執行緒」。</span><span class="sxs-lookup"><span data-stu-id="99f8e-115">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="99f8e-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="99f8e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99f8e-117">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="99f8e-117">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="99f8e-118">描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="99f8e-118">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="99f8e-119">資源系結</span><span class="sxs-lookup"><span data-stu-id="99f8e-119">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="99f8e-120">根簽章</span><span class="sxs-lookup"><span data-stu-id="99f8e-120">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





