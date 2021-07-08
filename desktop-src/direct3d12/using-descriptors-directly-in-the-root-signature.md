---
title: 直接在根簽章中使用描述項
description: 若要避免需要經過描述項堆積，您可以直接將描述項放入根簽章中。
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9d459f3195a4cf722ea210edbe63e5c1bf3cc8
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489170"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a><span data-ttu-id="fa302-103">直接在根簽章中使用描述項</span><span class="sxs-lookup"><span data-stu-id="fa302-103">Using descriptors directly in the root signature</span></span>

<span data-ttu-id="fa302-104">若要避免需要經過描述項堆積，您可以直接將描述項放入根簽章中。</span><span class="sxs-lookup"><span data-stu-id="fa302-104">To avoid the need to go through a descriptor heap, you can put a descriptor directly into the root signature.</span></span> <span data-ttu-id="fa302-105">這些描述項會佔用根簽章中的大量空間 (請參閱) 的根簽章 [限制](/windows/win32/direct3d12/root-signature-limits) ，因此建議您謹慎使用。</span><span class="sxs-lookup"><span data-stu-id="fa302-105">These descriptors take up a lot of space in the root signature (see [Root signature limits](/windows/win32/direct3d12/root-signature-limits)), so we recommend that you use them sparingly.</span></span>

<span data-ttu-id="fa302-106">使用方式的範例是在根配置中放置一個常數緩衝區視圖， (CBV) 變更每個繪製。</span><span class="sxs-lookup"><span data-stu-id="fa302-106">An example usage would be to place in the root layout a constant buffer view (CBV) that is changing per draw.</span></span> <span data-ttu-id="fa302-107">如此一來，就不需要由應用程式每次繪製來配置描述元堆積空間 (並將描述項資料表指向描述項堆積) 的新位置。</span><span class="sxs-lookup"><span data-stu-id="fa302-107">That's so that descriptor heap space doesn't have to be allocated by the application per draw (and saves pointing a descriptor table at the new location in the descriptor heap).</span></span> <span data-ttu-id="fa302-108">藉由將某個內容放在根簽章中，應用程式只會將版本控制責任交給驅動程式;但那就是驅動程式已經有的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="fa302-108">By putting something in the root signature, the application is merely handing the versioning responsibility to the driver; but that's infrastructure that drivers already have.</span></span>

<span data-ttu-id="fa302-109">如果是使用極少資源的轉譯，則如果所有所需的描述項都可以直接放在根簽章中，就可能完全不需要描述項資料表/堆積用途。</span><span class="sxs-lookup"><span data-stu-id="fa302-109">For rendering that uses extremely few resources, descriptor table/heap use may not be needed at all if all of the needed descriptors can be placed directly in the root signature.</span></span>

<span data-ttu-id="fa302-110">這些是根簽章中唯一支援的描述項類型。</span><span class="sxs-lookup"><span data-stu-id="fa302-110">These are the only types of descriptors supported in the root signature.</span></span>

- <span data-ttu-id="fa302-111">常數緩衝區視圖 (CBVs) 。</span><span class="sxs-lookup"><span data-stu-id="fa302-111">Constant buffer view (CBVs).</span></span>
- <span data-ttu-id="fa302-112">著色器資源檢視 (SRVs) /未排序的存取權視圖 (UAVs 不需要格式轉換的緩衝區資源)  (不具類型的緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="fa302-112">Shader resource views (SRVs) / unordered access views (UAVs) of buffer resources where format conversion is not required (untyped buffers).</span></span> <span data-ttu-id="fa302-113">可以與根描述元系結的不具類型緩衝區的一些範例包括 `StructuredBuffer<type>` 、 `RWStructuredBuffer<type>` `ByteAddressBuffer` 和 `RWByteAddressBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="fa302-113">Some examples of untyped buffers that can be bound with root descriptors include `StructuredBuffer<type>`, `RWStructuredBuffer<type>`, `ByteAddressBuffer` and `RWByteAddressBuffer`.</span></span> <span data-ttu-id="fa302-114">具類型的緩衝區（例如 `Buffer<uint>` 和） `Buffer<float2>` 不能。</span><span class="sxs-lookup"><span data-stu-id="fa302-114">Typed buffers such as `Buffer<uint>` and `Buffer<float2>` can't.</span></span>
- <span data-ttu-id="fa302-115">在本機或全域根簽章中，raytracing 加速結構的 SRVs。</span><span class="sxs-lookup"><span data-stu-id="fa302-115">SRVs of raytracing acceleration structures, in local or global root signatures.</span></span> 

<span data-ttu-id="fa302-116">根目錄中的 UAV 不能有與其相關聯的計數器。</span><span class="sxs-lookup"><span data-stu-id="fa302-116">A UAV in the root cannot have counters associated with it.</span></span> <span data-ttu-id="fa302-117">根簽章中的描述項會顯示為個別個別的描述元， &mdash; 但無法動態建立索引。</span><span class="sxs-lookup"><span data-stu-id="fa302-117">Descriptors in the root signature appear each as individual separate descriptors&mdash;they cannot be dynamically indexed.</span></span>

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

<span data-ttu-id="fa302-118">在上述範例中， `mySceneData` 不能宣告為數組， `cbuffer mySceneData[2]` 如果它將會對應到根簽章中的描述元。</span><span class="sxs-lookup"><span data-stu-id="fa302-118">In the above example, `mySceneData` can't be declared as an array, as in `cbuffer mySceneData[2]` if it is going to be mapped onto a descriptor in the root signature.</span></span> <span data-ttu-id="fa302-119">這是因為根簽章不支援跨描述元索引。</span><span class="sxs-lookup"><span data-stu-id="fa302-119">That's because indexing across descriptors isn't supported in the root signature.</span></span> <span data-ttu-id="fa302-120">如有需要，您可以定義不同的個別常數緩衝區，並將它們定義為根簽章中的個別專案。</span><span class="sxs-lookup"><span data-stu-id="fa302-120">If desired, you can define separate individual constant buffers, and define them each as a separate entry in the root signature.</span></span> <span data-ttu-id="fa302-121">請注意，在上述的範圍中 `mySceneData` ，有一個陣列 `bar[2]` 。</span><span class="sxs-lookup"><span data-stu-id="fa302-121">Note that within `mySceneData` above, there is an array `bar[2]`.</span></span> <span data-ttu-id="fa302-122">在常數緩衝區內的動態索引是有效的，因為根簽章中的描述元所 &mdash; 表現的行為，就像是透過描述元堆積存取相同的描述項一樣。</span><span class="sxs-lookup"><span data-stu-id="fa302-122">Dynamic indexing within the constant buffer is valid&mdash;a descriptor in the root signature behaves just like the same descriptor would behave if it were accessed through a descriptor heap.</span></span> <span data-ttu-id="fa302-123">這與直接在根簽章中的內嵌常數（也像常數緩衝區一樣）相同，但不允許在內嵌常數內動態編制索引的條件約束，因此不允許這種情況 `bar[2]` 。</span><span class="sxs-lookup"><span data-stu-id="fa302-123">This is in contrast with inlining constants directly in the root signature, which also appears like a constant buffer, except with the constraint that dynamic indexing within the inlined constants is not permitted, so `bar[2]` wouldn't be allowed there.</span></span>

<span data-ttu-id="fa302-124">從 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面 (的這些 api) 適用于直接在根簽章上設定描述項。</span><span class="sxs-lookup"><span data-stu-id="fa302-124">These APIs (from the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting descriptors directly on the root signature.</span></span>

-   [<span data-ttu-id="fa302-125">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="fa302-125">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="fa302-126">**SetGraphicsRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="fa302-126">**SetGraphicsRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [<span data-ttu-id="fa302-127">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="fa302-127">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="fa302-128">**SetGraphicsRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="fa302-128">**SetGraphicsRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [<span data-ttu-id="fa302-129">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="fa302-129">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="fa302-130">**SetGraphicsRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="fa302-130">**SetGraphicsRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> <span data-ttu-id="fa302-131">Direct3D 12 沒有 *根描述元陣列* 的概念。</span><span class="sxs-lookup"><span data-stu-id="fa302-131">There's no concept of a *root descriptor array* in Direct3D 12.</span></span> <span data-ttu-id="fa302-132">描述項陣列只在描述元堆積中受到支援。</span><span class="sxs-lookup"><span data-stu-id="fa302-132">Descriptor arrays are supported only in descriptor heaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa302-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa302-133">Related topics</span></span>

* [<span data-ttu-id="fa302-134">根簽章</span><span class="sxs-lookup"><span data-stu-id="fa302-134">Root signatures</span></span>](root-signatures.md)
