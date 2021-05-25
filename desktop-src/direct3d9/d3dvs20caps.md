---
description: 頂點著色器的帽常數。 D3DCAPS9 的 VS20Caps 成員會使用這些常數。
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342943"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="c1a0c-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="c1a0c-104">D3DVS20CAPS</span></span>

<span data-ttu-id="c1a0c-105">頂點著色器的帽常數。</span><span class="sxs-lookup"><span data-stu-id="c1a0c-105">Vertex shader caps constants.</span></span> <span data-ttu-id="c1a0c-106">[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 VS20Caps 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="c1a0c-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="c1a0c-107">\#定義</span><span class="sxs-lookup"><span data-stu-id="c1a0c-107">\#define</span></span>                              | <span data-ttu-id="c1a0c-108">值</span><span class="sxs-lookup"><span data-stu-id="c1a0c-108">Value</span></span>          | <span data-ttu-id="c1a0c-109">描述</span><span class="sxs-lookup"><span data-stu-id="c1a0c-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a0c-110">D3DVS20CAPS \_ PREDICATION</span><span class="sxs-lookup"><span data-stu-id="c1a0c-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="c1a0c-111"> (1 << 0) </span><span class="sxs-lookup"><span data-stu-id="c1a0c-111">(1 << 0)</span></span> | <span data-ttu-id="c1a0c-112">支援指令 predication。</span><span class="sxs-lookup"><span data-stu-id="c1a0c-112">Instruction predication is supported.</span></span> <span data-ttu-id="c1a0c-113">請參閱[setp \_ 複合-vs](../direct3dhlsl/setp-comp---vs.md)</span><span class="sxs-lookup"><span data-stu-id="c1a0c-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="c1a0c-114">D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="c1a0c-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="c1a0c-115">24</span><span class="sxs-lookup"><span data-stu-id="c1a0c-115">24</span></span>             | <span data-ttu-id="c1a0c-116">動態流程式控制制指令的最大層級 ([break-vs](../direct3dhlsl/break---vs.md)、 [break \_ 複合-](../direct3dhlsl/break-comp---vs.md)vs、 [breakp-](../direct3dhlsl/breakp---vs.md)vs，如果是 pred 和) ，則為，如果是，則為複合[ \_ ](../direct3dhlsl/if-comp---vs.md) \_ 。 [](../direct3dhlsl/if-pred---vs.md)</span><span class="sxs-lookup"><span data-stu-id="c1a0c-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="c1a0c-117">D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="c1a0c-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="c1a0c-118">0</span><span class="sxs-lookup"><span data-stu-id="c1a0c-118">0</span></span>              | <span data-ttu-id="c1a0c-119">動態流程式控制制指令的最小層級 ([break-vs](../direct3dhlsl/break---vs.md)、 [break \_ 複合-](../direct3dhlsl/break-comp---vs.md)vs、 [breakp-](../direct3dhlsl/breakp---vs.md)vs，如果是 pred 和) ，則為，如果是複合的，則為[ \_ ](../direct3dhlsl/if-comp---vs.md) \_ 。 [](../direct3dhlsl/if-pred---vs.md)</span><span class="sxs-lookup"><span data-stu-id="c1a0c-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="c1a0c-120">D3DVS20 \_ MAX \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="c1a0c-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="c1a0c-121">32</span><span class="sxs-lookup"><span data-stu-id="c1a0c-121">32</span></span>             | <span data-ttu-id="c1a0c-122">支援的臨時暫存器數目上限。</span><span class="sxs-lookup"><span data-stu-id="c1a0c-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c1a0c-123">D3DVS20 \_ MIN \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="c1a0c-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="c1a0c-124">12</span><span class="sxs-lookup"><span data-stu-id="c1a0c-124">12</span></span>             | <span data-ttu-id="c1a0c-125">支援的臨時暫存器數目下限。</span><span class="sxs-lookup"><span data-stu-id="c1a0c-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c1a0c-126">D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="c1a0c-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="c1a0c-127">4</span><span class="sxs-lookup"><span data-stu-id="c1a0c-127">4</span></span>              | <span data-ttu-id="c1a0c-128">迴圈的最大深度[： vs](../direct3dhlsl/loop---vs.md) / [rep-](../direct3dhlsl/rep---vs.md) vs 和[call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md)指令。</span><span class="sxs-lookup"><span data-stu-id="c1a0c-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="c1a0c-129">D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="c1a0c-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="c1a0c-130">1</span><span class="sxs-lookup"><span data-stu-id="c1a0c-130">1</span></span>              | <span data-ttu-id="c1a0c-131">迴圈的最小深度[-vs](../direct3dhlsl/loop---vs.md) / [rep-](../direct3dhlsl/rep---vs.md) vs 和[call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md)指令。</span><span class="sxs-lookup"><span data-stu-id="c1a0c-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="c1a0c-132">常數資訊</span><span class="sxs-lookup"><span data-stu-id="c1a0c-132">Constant Information</span></span>



| <span data-ttu-id="c1a0c-133">需求</span><span class="sxs-lookup"><span data-stu-id="c1a0c-133">Requirement</span></span>                         | <span data-ttu-id="c1a0c-134">值</span><span class="sxs-lookup"><span data-stu-id="c1a0c-134">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="c1a0c-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c1a0c-135">Header</span></span>                   | <span data-ttu-id="c1a0c-136">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="c1a0c-136">d3d9caps.h</span></span> |
| <span data-ttu-id="c1a0c-137">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="c1a0c-137">Minimum operating system</span></span> | <span data-ttu-id="c1a0c-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c1a0c-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c1a0c-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1a0c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1a0c-140">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="c1a0c-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="c1a0c-141">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c1a0c-141">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
