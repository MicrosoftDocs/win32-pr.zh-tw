---
title: 直接在根簽章中使用描述項
description: 應用程式可以直接將描述項放在根簽章中，以避免需要經過描述元堆積。
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548454"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a><span data-ttu-id="74daf-103">直接在根簽章中使用描述項</span><span class="sxs-lookup"><span data-stu-id="74daf-103">Using descriptors directly in the root signature</span></span>

<span data-ttu-id="74daf-104">應用程式可以直接將描述項放在根簽章中，以避免需要經過描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="74daf-104">Applications can put descriptors directly in the root signature to avoid having to go through a descriptor heap.</span></span> <span data-ttu-id="74daf-105">這些描述項會在根簽章中佔用大量空間 (請參閱) 的根簽章限制一節，讓應用程式必須謹慎使用它們。</span><span class="sxs-lookup"><span data-stu-id="74daf-105">These descriptors take a lot of space in the root signature (see the root signature limits section), so applications have to use them sparingly.</span></span>

<span data-ttu-id="74daf-106">使用方式的範例是將常數緩衝區視圖 (CBV，以在根配置中變更每個繪圖的) ，如此一來，應用程式就不需要配置描述元堆積空間，如此一來，應用程式就不需要為每個 (繪圖配置描述中繼資料表，然後將描述中繼資料表指向描述項堆積) 的新位置。</span><span class="sxs-lookup"><span data-stu-id="74daf-106">An example usage would be to place a constant buffer views (CBV) that is changing per draw in the root layout so that descriptor heap space doesn't have to be allocated by the application per draw (and save pointing a descriptor table at the new location in the descriptor heap).</span></span> <span data-ttu-id="74daf-107">藉由將某個內容放在根簽章中，應用程式只會將版本控制責任交給驅動程式，但這是它們已經有的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="74daf-107">By putting something in the root signature, the application is merely handing the versioning responsibility to the driver, but this is infrastructure that they already have.</span></span>

<span data-ttu-id="74daf-108">如果是使用極少資源的轉譯，則如果所有所需的描述項都可以直接放在根簽章中，就可能完全不需要描述項資料表/堆積用途。</span><span class="sxs-lookup"><span data-stu-id="74daf-108">For rendering that uses extremely few resources, descriptor table/heap use may not be needed at all if all the needed descriptors can be placed directly in the root signature.</span></span>

<span data-ttu-id="74daf-109">根簽章中唯一支援的描述項類型為：</span><span class="sxs-lookup"><span data-stu-id="74daf-109">The only types of descriptors supported in the root signature are:</span></span>
- <span data-ttu-id="74daf-110">CBVs.</span><span class="sxs-lookup"><span data-stu-id="74daf-110">CBVs.</span></span>
- <span data-ttu-id="74daf-111">著色器資源檢視 (SRVs) /Unordered 存取權視圖 (UAVs) 緩衝區資源，其中 SRV/UAV 格式只包含32位 FLOAT/UINT/聖中的元件 (沒有格式轉換) 。</span><span class="sxs-lookup"><span data-stu-id="74daf-111">Shader Resource Views (SRVs)/Unordered Access Views (UAVs) of buffer resources where the SRV/UAV format contains only 32 bit FLOAT/UINT/SINT components (there is no format conversion).</span></span>
- <span data-ttu-id="74daf-112">在本機或全域根簽章中，raytracing 加速結構的 SRVs。</span><span class="sxs-lookup"><span data-stu-id="74daf-112">SRVs of raytracing acceleration structures, in local or global root signatures.</span></span> 

<span data-ttu-id="74daf-113">根目錄中的 UAVs 不能有與其相關聯的計數器。</span><span class="sxs-lookup"><span data-stu-id="74daf-113">UAVs in the root cannot have counters associated with them.</span></span> <span data-ttu-id="74daf-114">根簽章中的描述項會顯示為個別個別的描述元， &mdash; 但無法動態建立索引。</span><span class="sxs-lookup"><span data-stu-id="74daf-114">Descriptors in the root signature appear each as individual separate descriptors&mdash;they cannot be dynamically indexed.</span></span>

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

<span data-ttu-id="74daf-115">在上述範例中， `mySceneData` 無法宣告為數組，例如， `cbuffer mySceneData[2]` 如果它會對應至根簽章中的描述元，則在根簽章中不支援跨描述元編制索引。</span><span class="sxs-lookup"><span data-stu-id="74daf-115">In the above example, `mySceneData` cannot be declared as an array, as in `cbuffer mySceneData[2]` if it is going to be mapped onto a descriptor in the root signature, since indexing across descriptors is not supported in the root signature.</span></span> <span data-ttu-id="74daf-116">應用程式可以定義個別的個別常數緩衝區，並在需要時將它們定義為根簽章中的個別專案。</span><span class="sxs-lookup"><span data-stu-id="74daf-116">The application can define separate individual constant buffers and define them each as a separate entry in the root signature if desired.</span></span> <span data-ttu-id="74daf-117">請注意，在上述的範圍中 `mySceneData` ，有一個陣列 `bar[2]` 。</span><span class="sxs-lookup"><span data-stu-id="74daf-117">Note that within `mySceneData` above, there is an array `bar[2]`.</span></span> <span data-ttu-id="74daf-118">常數緩衝區內的動態索引是有效的-根簽章中的描述項的行為就像是透過描述元堆積存取相同的描述項。</span><span class="sxs-lookup"><span data-stu-id="74daf-118">Dynamic indexing within the constant buffer is valid - a descriptor in the root signature behaves just like the same descriptor would behave if accessed through a descriptor heap.</span></span> <span data-ttu-id="74daf-119">這與直接在根簽章中的內嵌常數不同，它也像常數緩衝區一樣出現，但條件約束不允許內嵌常數內的動態索引編制，因此不允許這種情況 `bar[2]` 。</span><span class="sxs-lookup"><span data-stu-id="74daf-119">This is in contrast with inlining constants directly in the root signature, which also appears like a constant buffer except with the constraint that dynamic indexing within the inlined constants is not permitted, so `bar[2]` would not be allowed there.</span></span>

<span data-ttu-id="74daf-120">下列 (自 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面的 api) 適用于直接在根簽章上設定描述項：</span><span class="sxs-lookup"><span data-stu-id="74daf-120">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting descriptors directly on the root signature:</span></span>

-   [<span data-ttu-id="74daf-121">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="74daf-121">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="74daf-122">**SetGraphicsRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="74daf-122">**SetGraphicsRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [<span data-ttu-id="74daf-123">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="74daf-123">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="74daf-124">**SetGraphicsRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="74daf-124">**SetGraphicsRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [<span data-ttu-id="74daf-125">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="74daf-125">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="74daf-126">**SetGraphicsRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="74daf-126">**SetGraphicsRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> <span data-ttu-id="74daf-127">Direct3D 12 沒有「根描述元陣列」的概念。</span><span class="sxs-lookup"><span data-stu-id="74daf-127">There is no concept of a "root descriptor array" in Direct3D 12.</span></span> <span data-ttu-id="74daf-128">描述項陣列只在描述元堆積中受到支援。</span><span class="sxs-lookup"><span data-stu-id="74daf-128">Descriptor arrays are only supported in descriptor heaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74daf-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="74daf-129">Related topics</span></span>

[<span data-ttu-id="74daf-130">根簽章</span><span class="sxs-lookup"><span data-stu-id="74daf-130">Root Signatures</span></span>](root-signatures.md)
