---
title: 直接在根簽章中使用常數
description: 應用程式可以在根簽章中定義根常數，每個常數都是一組32位值。 它們會以高階的陰影語言顯示 (HLSL) 作為常數緩衝區。 請注意，記錄原因的常數緩衝區會視為4x32 位值的集合。
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104892"
---
# <a name="using-constants-directly-in-the-root-signature"></a><span data-ttu-id="1c3a2-105">直接在根簽章中使用常數</span><span class="sxs-lookup"><span data-stu-id="1c3a2-105">Using Constants Directly in the Root Signature</span></span>

<span data-ttu-id="1c3a2-106">應用程式可以在根簽章中定義根常數，每個常數都是一組32位值。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-106">Applications can define root constants in the root signature, each as a set of 32-bit values.</span></span> <span data-ttu-id="1c3a2-107">它們會以高階的陰影語言顯示 (HLSL) 作為常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-107">They appear in High Level Shading Language (HLSL) as a constant buffer.</span></span> <span data-ttu-id="1c3a2-108">請注意，記錄原因的常數緩衝區會視為4x32 位值的集合。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-108">Note that constant buffers for historical reasons are viewed as sets of 4x32-bit values.</span></span>

<span data-ttu-id="1c3a2-109">每一組使用者常數都會被視為32位值的純量陣列，可動態編制索引，而且是從著色器的唯讀。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-109">Each set of user constants is treated as a scalar array of 32 -bit values, dynamically indexable and read-only from the shader.</span></span> <span data-ttu-id="1c3a2-110">指定根常數集合的超出範圍索引會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-110">Out of bounds indexing a given set of root constants produces undefined results.</span></span> <span data-ttu-id="1c3a2-111">在 HLSL 中，可以提供資料結構定義給使用者常數，以提供它們類型。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-111">In HLSL, data structure definitions can be provided for the user constants to give them types.</span></span> <span data-ttu-id="1c3a2-112">例如，如果根簽章定義4個根常數的集合，HLSL 可以在其上重迭下列結構。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-112">For example, if the root signature defines a set of 4 root constants, HLSL can overlay the following structure on them.</span></span>

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

<span data-ttu-id="1c3a2-113">因為不支援根簽章空間中的動態索引編制，所以不允許在會對應至根常數的常數緩衝區中使用陣列。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-113">Arrays are not permitted in constant buffers that get mapped onto root constants since dynamic indexing in the root signature space is not supported.</span></span> <span data-ttu-id="1c3a2-114">例如，在常數緩衝區中有一個專案（例如）是不正確 `float myArray[2];` 。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-114">For example, it is invalid to have an entry in the constant buffer like `float myArray[2];`.</span></span> <span data-ttu-id="1c3a2-115">對應至根常數的常數緩衝區本身不能是陣列;因此，對應 `cbuffer myCBArray[2]` 至根常數是不正確。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-115">A constant buffer that is mapped to root constants cannot itself be an array; therefore, it is invalid to map `cbuffer myCBArray[2]` into root constants.</span></span>

<span data-ttu-id="1c3a2-116">可以部分設定常數。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-116">Constants can be partially set.</span></span> <span data-ttu-id="1c3a2-117">例如，如果根簽章在 *RootTableBindSlot* 2 定義 4 32 位的值，則可以一次設定四個常數的任何子集， (其他常數保持不變) 。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-117">For example, if the root signature defines four 32-bit values at *RootTableBindSlot* 2, then any subset of the four constants can be set at a time (the others remain unchanged).</span></span> <span data-ttu-id="1c3a2-118">這在會繼承根簽章狀態並可部分變更的組合中很有用。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-118">This can be useful in bundles that inherit root signature state and can partially change it.</span></span>

<span data-ttu-id="1c3a2-119">設定常數時，請小心著色器預期的常數緩衝區配置。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-119">When setting constants be careful of the constant buffer layout expected by the shader.</span></span> <span data-ttu-id="1c3a2-120">例如，常數可以填補至 `vec4` 界限。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-120">It is possible that constants are padded to `vec4` boundaries, for example.</span></span> <span data-ttu-id="1c3a2-121">若要驗證預期的版面配置，請從 HLSL 著色器檢查反映資訊。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-121">To verify the layout expected, check the reflection information from the HLSL shader.</span></span>

<span data-ttu-id="1c3a2-122">下列 (自 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面的 api) 用於直接在根簽章上設定常數：</span><span class="sxs-lookup"><span data-stu-id="1c3a2-122">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting constants directly on the root signature:</span></span>

-   [<span data-ttu-id="1c3a2-123">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="1c3a2-123">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [<span data-ttu-id="1c3a2-124">**SetGraphicsRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="1c3a2-124">**SetGraphicsRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [<span data-ttu-id="1c3a2-125">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="1c3a2-125">**SetComputeRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="1c3a2-126">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="1c3a2-126">**SetComputeRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

<span data-ttu-id="1c3a2-127">此外，請參閱 [**D3D12 \_ 根 \_ 常數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) 結構。</span><span class="sxs-lookup"><span data-stu-id="1c3a2-127">Also, refer to the [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c3a2-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c3a2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c3a2-129">根簽章</span><span class="sxs-lookup"><span data-stu-id="1c3a2-129">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




