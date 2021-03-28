---
title: 'callc (sm4-asm) '
description: 有條件地呼叫以程式中的標籤 l 出現位置標示的副程式。
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990759"
---
# <a name="callc-sm4---asm"></a><span data-ttu-id="b0f0f-103">callc (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="b0f0f-103">callc (sm4 - asm)</span></span>

<span data-ttu-id="b0f0f-104">有條件地呼叫在程式中出現卷 **標 \# l** 的位置所標示的副程式。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-104">Conditionally calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="b0f0f-105">callc { \_ z </span><span class="sxs-lookup"><span data-stu-id="b0f0f-105">callc{\_z</span></span>\|<span data-ttu-id="b0f0f-106">\_nz} src0。選取 \_ 元件，l\#</span><span class="sxs-lookup"><span data-stu-id="b0f0f-106">\_nz} src0.select\_component, l\#</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="b0f0f-107">項目</span><span class="sxs-lookup"><span data-stu-id="b0f0f-107">Item</span></span>                                                            | <span data-ttu-id="b0f0f-108">描述</span><span class="sxs-lookup"><span data-stu-id="b0f0f-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="b0f0f-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b0f0f-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b0f0f-110">\[在 \] 測試條件的元件中。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-110">\[in\] The component on which to test the condition.</span></span><br/> |
| <span data-ttu-id="b0f0f-111"><span id="l_"></span><span id="L_"></span>*我\#*</span><span class="sxs-lookup"><span data-stu-id="b0f0f-111"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/>      | <span data-ttu-id="b0f0f-112">\[在 \] 副程式的標籤中。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-112">\[in\] The label of the subroutine.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b0f0f-113">備註</span><span class="sxs-lookup"><span data-stu-id="b0f0f-113">Remarks</span></span>

<span data-ttu-id="b0f0f-114">當遇到 [ret](ret--sm4---asm-.md) 時，會在這個呼叫之後，將執行傳回給指令。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-114">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="b0f0f-115">標記格式包含著色器中對應標籤的位移，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-115">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="b0f0f-116">下列範例顯示呼叫指令。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-116">The following example shows the call instruction.</span></span>


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a><span data-ttu-id="b0f0f-117">限制</span><span class="sxs-lookup"><span data-stu-id="b0f0f-117">Restrictions</span></span>

-   <span data-ttu-id="b0f0f-118">副程式可以嵌套32深度。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-118">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="b0f0f-119">傳回位址堆疊是由實作為透明管理。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-119">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="b0f0f-120">如果傳回位址堆疊上已有32個專案，且發出 **呼叫** ，則會略過呼叫。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-120">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="b0f0f-121">沒有自動參數堆疊。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-121">There is no automatic parameter stack.</span></span> <span data-ttu-id="b0f0f-122">應用程式可以使用可編制索引的臨時暫存器陣列 (x \# \[ \]) ，以手動方式執行堆疊。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-122">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="b0f0f-123">但是，不會顯示副程式呼叫傳回位址，而且會與應用程式所完成的任何手動堆疊管理進行迭。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-123">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="b0f0f-124">不允許對 *l \#* 參數進行索引。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-124">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="b0f0f-125">*Src0* 提供的32位暫存器會在位層級進行測試。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-125">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="b0f0f-126">如果有任何位為非零值， **callc \_ nz** 將會執行呼叫。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-126">If any bit is nonzero, **callc\_nz** will perform the call.</span></span> <span data-ttu-id="b0f0f-127">如果所有位都是零， **callc \_ z** 將會執行呼叫。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-127">If all bits are zero, **callc\_z** will perform the call.</span></span>
-   <span data-ttu-id="b0f0f-128">不允許遞迴。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-128">Recursion is not permitted.</span></span>

<span data-ttu-id="b0f0f-129">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="b0f0f-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b0f0f-130">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="b0f0f-130">Vertex Shader</span></span> | <span data-ttu-id="b0f0f-131">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="b0f0f-131">Geometry Shader</span></span> | <span data-ttu-id="b0f0f-132">像素著色器</span><span class="sxs-lookup"><span data-stu-id="b0f0f-132">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b0f0f-133">x</span><span class="sxs-lookup"><span data-stu-id="b0f0f-133">x</span></span>             | <span data-ttu-id="b0f0f-134">x</span><span class="sxs-lookup"><span data-stu-id="b0f0f-134">x</span></span>               | <span data-ttu-id="b0f0f-135">x</span><span class="sxs-lookup"><span data-stu-id="b0f0f-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b0f0f-136">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="b0f0f-136">Minimum Shader Model</span></span>

<span data-ttu-id="b0f0f-137">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="b0f0f-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b0f0f-138">著色器模型</span><span class="sxs-lookup"><span data-stu-id="b0f0f-138">Shader Model</span></span>                                              | <span data-ttu-id="b0f0f-139">支援</span><span class="sxs-lookup"><span data-stu-id="b0f0f-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b0f0f-140">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b0f0f-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b0f0f-141">是</span><span class="sxs-lookup"><span data-stu-id="b0f0f-141">yes</span></span>       |
| [<span data-ttu-id="b0f0f-142">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="b0f0f-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b0f0f-143">是</span><span class="sxs-lookup"><span data-stu-id="b0f0f-143">yes</span></span>       |
| [<span data-ttu-id="b0f0f-144">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="b0f0f-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b0f0f-145">是</span><span class="sxs-lookup"><span data-stu-id="b0f0f-145">yes</span></span>       |
| [<span data-ttu-id="b0f0f-146">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b0f0f-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b0f0f-147">不可以</span><span class="sxs-lookup"><span data-stu-id="b0f0f-147">no</span></span>        |
| [<span data-ttu-id="b0f0f-148">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b0f0f-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b0f0f-149">不可以</span><span class="sxs-lookup"><span data-stu-id="b0f0f-149">no</span></span>        |
| [<span data-ttu-id="b0f0f-150">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b0f0f-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b0f0f-151">不可以</span><span class="sxs-lookup"><span data-stu-id="b0f0f-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b0f0f-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0f0f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f0f-153">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="b0f0f-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





