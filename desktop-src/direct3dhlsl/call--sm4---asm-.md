---
title: '呼叫 (sm4-asm) '
description: 呼叫程式中出現標籤 l 時所標示的副程式。
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679132"
---
# <a name="call-sm4---asm"></a><span data-ttu-id="aec8e-103">呼叫 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="aec8e-103">call (sm4 - asm)</span></span>

<span data-ttu-id="aec8e-104">呼叫在程式中顯示標籤 **l \#** 的位置所標示的副程式。</span><span class="sxs-lookup"><span data-stu-id="aec8e-104">Calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="aec8e-105">呼叫 l\#</span><span class="sxs-lookup"><span data-stu-id="aec8e-105">call l\#</span></span> |
|----------|



 



| <span data-ttu-id="aec8e-106">項目</span><span class="sxs-lookup"><span data-stu-id="aec8e-106">Item</span></span>                                                       | <span data-ttu-id="aec8e-107">描述</span><span class="sxs-lookup"><span data-stu-id="aec8e-107">Description</span></span>                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="aec8e-108"><span id="l_"></span><span id="L_"></span>*我\#*</span><span class="sxs-lookup"><span data-stu-id="aec8e-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="aec8e-109">\[在 \] 副程式的標籤中。</span><span class="sxs-lookup"><span data-stu-id="aec8e-109">\[in\] The label of the subroutine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aec8e-110">備註</span><span class="sxs-lookup"><span data-stu-id="aec8e-110">Remarks</span></span>

<span data-ttu-id="aec8e-111">當遇到 [ret](ret--sm4---asm-.md) 時，會在這個呼叫之後，將執行傳回給指令。</span><span class="sxs-lookup"><span data-stu-id="aec8e-111">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="aec8e-112">標記格式包含著色器中對應標籤的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="aec8e-112">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="aec8e-113">下列範例顯示呼叫指令。</span><span class="sxs-lookup"><span data-stu-id="aec8e-113">The following example shows the call instruction.</span></span>


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a><span data-ttu-id="aec8e-114">限制</span><span class="sxs-lookup"><span data-stu-id="aec8e-114">Restrictions</span></span>

-   <span data-ttu-id="aec8e-115">副程式可以嵌套32深度。</span><span class="sxs-lookup"><span data-stu-id="aec8e-115">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="aec8e-116">傳回位址堆疊是由實作為透明管理。</span><span class="sxs-lookup"><span data-stu-id="aec8e-116">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="aec8e-117">如果傳回位址堆疊上已有32個專案，且發出 **呼叫** ，則會略過呼叫。</span><span class="sxs-lookup"><span data-stu-id="aec8e-117">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="aec8e-118">沒有自動參數堆疊。</span><span class="sxs-lookup"><span data-stu-id="aec8e-118">There is no automatic parameter stack.</span></span> <span data-ttu-id="aec8e-119">應用程式可以使用可編制索引的臨時暫存器陣列 (x \# \[ \]) ，以手動方式執行堆疊。</span><span class="sxs-lookup"><span data-stu-id="aec8e-119">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="aec8e-120">但是，不會顯示副程式呼叫傳回位址，而且會與應用程式所完成的任何手動堆疊管理進行迭。</span><span class="sxs-lookup"><span data-stu-id="aec8e-120">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="aec8e-121">不允許對 *l \#* 參數進行索引。</span><span class="sxs-lookup"><span data-stu-id="aec8e-121">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="aec8e-122">不允許遞迴。</span><span class="sxs-lookup"><span data-stu-id="aec8e-122">Recursion is not permitted.</span></span>

<span data-ttu-id="aec8e-123">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="aec8e-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aec8e-124">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="aec8e-124">Vertex Shader</span></span> | <span data-ttu-id="aec8e-125">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="aec8e-125">Geometry Shader</span></span> | <span data-ttu-id="aec8e-126">像素著色器</span><span class="sxs-lookup"><span data-stu-id="aec8e-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aec8e-127">x</span><span class="sxs-lookup"><span data-stu-id="aec8e-127">x</span></span>             | <span data-ttu-id="aec8e-128">x</span><span class="sxs-lookup"><span data-stu-id="aec8e-128">x</span></span>               | <span data-ttu-id="aec8e-129">x</span><span class="sxs-lookup"><span data-stu-id="aec8e-129">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aec8e-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="aec8e-130">Minimum Shader Model</span></span>

<span data-ttu-id="aec8e-131">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="aec8e-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aec8e-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="aec8e-132">Shader Model</span></span>                                              | <span data-ttu-id="aec8e-133">支援</span><span class="sxs-lookup"><span data-stu-id="aec8e-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aec8e-134">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="aec8e-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aec8e-135">是</span><span class="sxs-lookup"><span data-stu-id="aec8e-135">yes</span></span>       |
| [<span data-ttu-id="aec8e-136">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="aec8e-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aec8e-137">是</span><span class="sxs-lookup"><span data-stu-id="aec8e-137">yes</span></span>       |
| [<span data-ttu-id="aec8e-138">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="aec8e-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aec8e-139">是</span><span class="sxs-lookup"><span data-stu-id="aec8e-139">yes</span></span>       |
| [<span data-ttu-id="aec8e-140">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aec8e-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aec8e-141">不可以</span><span class="sxs-lookup"><span data-stu-id="aec8e-141">no</span></span>        |
| [<span data-ttu-id="aec8e-142">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aec8e-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aec8e-143">不可以</span><span class="sxs-lookup"><span data-stu-id="aec8e-143">no</span></span>        |
| [<span data-ttu-id="aec8e-144">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aec8e-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aec8e-145">不可以</span><span class="sxs-lookup"><span data-stu-id="aec8e-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aec8e-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="aec8e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec8e-147">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aec8e-147">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





