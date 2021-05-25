---
description: 驅動程式範本功能旗標。
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343053"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="ea366-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="ea366-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="ea366-104">驅動程式範本功能旗標。</span><span class="sxs-lookup"><span data-stu-id="ea366-104">Driver stencil capability flags.</span></span>



| <span data-ttu-id="ea366-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="ea366-105">\#define</span></span>                 | <span data-ttu-id="ea366-106">值</span><span class="sxs-lookup"><span data-stu-id="ea366-106">Value</span></span>       | <span data-ttu-id="ea366-107">描述</span><span class="sxs-lookup"><span data-stu-id="ea366-107">Description</span></span>                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea366-108">D3DSTENCILCAPS \_ 保留</span><span class="sxs-lookup"><span data-stu-id="ea366-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="ea366-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="ea366-109">0x00000001L</span></span> | <span data-ttu-id="ea366-110">請勿更新樣板緩衝區中的專案。</span><span class="sxs-lookup"><span data-stu-id="ea366-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="ea366-111">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="ea366-111">This is the default value.</span></span>                             |
| <span data-ttu-id="ea366-112">D3DSTENCILCAPS \_ 零</span><span class="sxs-lookup"><span data-stu-id="ea366-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="ea366-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="ea366-113">0x00000002L</span></span> | <span data-ttu-id="ea366-114">將樣板緩衝區專案設定為0。</span><span class="sxs-lookup"><span data-stu-id="ea366-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="ea366-115">D3DSTENCILCAPS \_ REPLACE</span><span class="sxs-lookup"><span data-stu-id="ea366-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="ea366-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="ea366-116">0x00000004L</span></span> | <span data-ttu-id="ea366-117">將樣板緩衝區專案取代為參考值。</span><span class="sxs-lookup"><span data-stu-id="ea366-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="ea366-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="ea366-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="ea366-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="ea366-119">0x00000008L</span></span> | <span data-ttu-id="ea366-120">將樣板緩衝區專案遞增，固定為最大值。</span><span class="sxs-lookup"><span data-stu-id="ea366-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="ea366-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="ea366-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="ea366-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="ea366-122">0x00000010L</span></span> | <span data-ttu-id="ea366-123">遞減樣板緩衝區專案，固定為零。</span><span class="sxs-lookup"><span data-stu-id="ea366-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="ea366-124">D3DSTENCILCAPS \_ 反轉</span><span class="sxs-lookup"><span data-stu-id="ea366-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="ea366-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="ea366-125">0x00000020L</span></span> | <span data-ttu-id="ea366-126">反轉樣板緩衝區專案中的位。</span><span class="sxs-lookup"><span data-stu-id="ea366-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="ea366-127">D3DSTENCILCAPS \_ 增量</span><span class="sxs-lookup"><span data-stu-id="ea366-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="ea366-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="ea366-128">0x00000040L</span></span> | <span data-ttu-id="ea366-129">如果新值超過最大值，則將樣板緩衝區專案遞增，並將其換成零。</span><span class="sxs-lookup"><span data-stu-id="ea366-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="ea366-130">D3DSTENCILCAPS \_ operators.decr</span><span class="sxs-lookup"><span data-stu-id="ea366-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="ea366-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="ea366-131">0x00000080L</span></span> | <span data-ttu-id="ea366-132">遞減樣板緩衝區專案，如果新值小於零，則會換行到最大值。</span><span class="sxs-lookup"><span data-stu-id="ea366-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="ea366-133">D3DSTENCILCAPS \_ TWOSIDED</span><span class="sxs-lookup"><span data-stu-id="ea366-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="ea366-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="ea366-134">0x00000100L</span></span> | <span data-ttu-id="ea366-135">裝置支援雙面樣板。</span><span class="sxs-lookup"><span data-stu-id="ea366-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="ea366-136">樣板-緩衝區專案是整數值，範圍從0到2ⁿ-1，其中 n 是樣板緩衝區的位深度。</span><span class="sxs-lookup"><span data-stu-id="ea366-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="ea366-137">[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 StencilCaps 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="ea366-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="ea366-138">常數資訊</span><span class="sxs-lookup"><span data-stu-id="ea366-138">Constant Information</span></span>



| <span data-ttu-id="ea366-139">需求</span><span class="sxs-lookup"><span data-stu-id="ea366-139">Requirement</span></span>                         | <span data-ttu-id="ea366-140">值</span><span class="sxs-lookup"><span data-stu-id="ea366-140">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="ea366-141">標頭</span><span class="sxs-lookup"><span data-stu-id="ea366-141">Header</span></span>                   | <span data-ttu-id="ea366-142">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="ea366-142">d3d9caps.h</span></span> |
| <span data-ttu-id="ea366-143">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="ea366-143">Minimum operating system</span></span> | <span data-ttu-id="ea366-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ea366-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ea366-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea366-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea366-146">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="ea366-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



