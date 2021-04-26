---
description: 圖元著色器功能旗標。
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2326b8f5066d34087fb543c7771a0cd547b98f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995265"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="90335-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="90335-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="90335-104">圖元著色器功能旗標。</span><span class="sxs-lookup"><span data-stu-id="90335-104">Pixel shader capability flags.</span></span>



| <span data-ttu-id="90335-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="90335-105">\#define</span></span>                                     | <span data-ttu-id="90335-106">值</span><span class="sxs-lookup"><span data-stu-id="90335-106">Value</span></span>          | <span data-ttu-id="90335-107">描述</span><span class="sxs-lookup"><span data-stu-id="90335-107">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90335-108">D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="90335-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="90335-109"> (1 << 0) </span><span class="sxs-lookup"><span data-stu-id="90335-109">(1 << 0)</span></span> | <span data-ttu-id="90335-110">支援任意 swizzling。</span><span class="sxs-lookup"><span data-stu-id="90335-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="90335-111">D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="90335-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="90335-112"> (1 << 1) </span><span class="sxs-lookup"><span data-stu-id="90335-112">(1 << 1)</span></span> | <span data-ttu-id="90335-113">支援漸層指令。</span><span class="sxs-lookup"><span data-stu-id="90335-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="90335-114">D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION</span><span class="sxs-lookup"><span data-stu-id="90335-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="90335-115"> (1 << 2) </span><span class="sxs-lookup"><span data-stu-id="90335-115">(1 << 2)</span></span> | <span data-ttu-id="90335-116">支援指令 predication。</span><span class="sxs-lookup"><span data-stu-id="90335-116">Instruction predication is supported.</span></span> <span data-ttu-id="90335-117">請參閱 [setp \_ 的複合-ps](../direct3dhlsl/setp-comp---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="90335-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="90335-118">D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="90335-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="90335-119"> (1 << 3) </span><span class="sxs-lookup"><span data-stu-id="90335-119">(1 << 3)</span></span> | <span data-ttu-id="90335-120">每個指令的相依讀取數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="90335-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="90335-121">D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="90335-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="90335-122"> (1 << 4) </span><span class="sxs-lookup"><span data-stu-id="90335-122">(1 << 4)</span></span> | <span data-ttu-id="90335-123">Tex 指令數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="90335-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="90335-124">D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="90335-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="90335-125">24</span><span class="sxs-lookup"><span data-stu-id="90335-125">24</span></span>             | <span data-ttu-id="90335-126">動態流程式控制制指令的最大層級 (break、breakc、ifc) 。</span><span class="sxs-lookup"><span data-stu-id="90335-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="90335-127">D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="90335-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="90335-128">0</span><span class="sxs-lookup"><span data-stu-id="90335-128">0</span></span>              | <span data-ttu-id="90335-129">動態流程式控制制指令的最小層級 (break、breakc、ifc) 。</span><span class="sxs-lookup"><span data-stu-id="90335-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="90335-130">D3DPS20 \_ MAX \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="90335-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="90335-131">32</span><span class="sxs-lookup"><span data-stu-id="90335-131">32</span></span>             | <span data-ttu-id="90335-132">驅動程式最多可支援此許多暫存註冊。</span><span class="sxs-lookup"><span data-stu-id="90335-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="90335-133">D3DPS20 \_ MIN \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="90335-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="90335-134">12</span><span class="sxs-lookup"><span data-stu-id="90335-134">12</span></span>             | <span data-ttu-id="90335-135">驅動程式至少會支援這個許多暫存註冊。</span><span class="sxs-lookup"><span data-stu-id="90335-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="90335-136">D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="90335-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="90335-137">4</span><span class="sxs-lookup"><span data-stu-id="90335-137">4</span></span>              | <span data-ttu-id="90335-138">迴圈的最大深度[： vs](../direct3dhlsl/loop---vs.md) / [rep-](../direct3dhlsl/rep---vs.md) vs 和[call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md)指令。</span><span class="sxs-lookup"><span data-stu-id="90335-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="90335-139">D3DPS20 \_ MIN \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="90335-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="90335-140">1</span><span class="sxs-lookup"><span data-stu-id="90335-140">1</span></span>              | <span data-ttu-id="90335-141">迴圈的最小深度[-vs](../direct3dhlsl/loop---vs.md) / [rep-](../direct3dhlsl/rep---vs.md) vs 和[call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md)指令。</span><span class="sxs-lookup"><span data-stu-id="90335-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="90335-142">D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="90335-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="90335-143">512</span><span class="sxs-lookup"><span data-stu-id="90335-143">512</span></span>            | <span data-ttu-id="90335-144">驅動程式最多可支援此許多指示。</span><span class="sxs-lookup"><span data-stu-id="90335-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="90335-145">D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="90335-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="90335-146">96</span><span class="sxs-lookup"><span data-stu-id="90335-146">96</span></span>             | <span data-ttu-id="90335-147">驅動程式至少會支援此許多指示。</span><span class="sxs-lookup"><span data-stu-id="90335-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="90335-148">這些常數會由 D3DCAPS9 的 D3DPSHADERCAPS2 \_ 0 成員使用[](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)。</span><span class="sxs-lookup"><span data-stu-id="90335-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="90335-149">常數資訊</span><span class="sxs-lookup"><span data-stu-id="90335-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="90335-150">標頭</span><span class="sxs-lookup"><span data-stu-id="90335-150">Header</span></span>                   | <span data-ttu-id="90335-151">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="90335-151">d3d9caps.h</span></span> |
| <span data-ttu-id="90335-152">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="90335-152">Minimum operating system</span></span> | <span data-ttu-id="90335-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="90335-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="90335-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="90335-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90335-155">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="90335-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="90335-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="90335-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
