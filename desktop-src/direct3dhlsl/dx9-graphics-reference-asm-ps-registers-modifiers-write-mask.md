---
title: 目的地註冊寫入遮罩
description: 寫入遮罩可控制在完成指令之後，要寫入目的地暫存器的哪些元件。
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932583"
---
# <a name="destination-register-write-mask"></a><span data-ttu-id="02dee-103">目的地註冊寫入遮罩</span><span class="sxs-lookup"><span data-stu-id="02dee-103">Destination Register Write Mask</span></span>

<span data-ttu-id="02dee-104">寫入遮罩可控制在完成指令之後，要寫入目的地暫存器的哪些元件。</span><span class="sxs-lookup"><span data-stu-id="02dee-104">A write mask controls which components of a destination register are written after an instruction is completed.</span></span> <span data-ttu-id="02dee-105">只要元件的順序為 rgba 或 xyzw，就可以使用輸出寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="02dee-105">An output write mask is allowed as long as the components are in the order of .rgba or .xyzw.</span></span> <span data-ttu-id="02dee-106">也就是說，rba 和. xw 是有效的遮罩。</span><span class="sxs-lookup"><span data-stu-id="02dee-106">That is, .rba and .xw are valid masks.</span></span> <span data-ttu-id="02dee-107">材質暫存器有一組規則，而非材質暫存器有另一組規則。</span><span class="sxs-lookup"><span data-stu-id="02dee-107">Texture registers have one set of rules and non-texture registers have another set of rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="02dee-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="02dee-108">Syntax</span></span>



| <span data-ttu-id="02dee-109">writemask</span><span class="sxs-lookup"><span data-stu-id="02dee-109">dst.writemask</span></span> |
|---------------|



 

<span data-ttu-id="02dee-110">其中</span><span class="sxs-lookup"><span data-stu-id="02dee-110">where</span></span>

-   <span data-ttu-id="02dee-111">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="02dee-111">dst is a destination register.</span></span>
-   <span data-ttu-id="02dee-112">writemask 是任一組的遮罩序列： (x、y、z、w) 或 (紅色、綠色、藍色、Alpha) 。</span><span class="sxs-lookup"><span data-stu-id="02dee-112">writemask is a sequence of masks from either set: (x,y,z,w) or (red, green, blue, alpha).</span></span>

## <a name="remarks"></a><span data-ttu-id="02dee-113">備註</span><span class="sxs-lookup"><span data-stu-id="02dee-113">Remarks</span></span>

<span data-ttu-id="02dee-114">以下是可用的目的地寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="02dee-114">The following destination write masks are available.</span></span>



| <span data-ttu-id="02dee-115">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="02dee-115">Pixel shader versions</span></span> | <span data-ttu-id="02dee-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="02dee-116">1\_1</span></span> | <span data-ttu-id="02dee-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="02dee-117">1\_2</span></span> | <span data-ttu-id="02dee-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="02dee-118">1\_3</span></span> | <span data-ttu-id="02dee-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="02dee-119">1\_4</span></span> | <span data-ttu-id="02dee-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="02dee-120">2\_0</span></span> | <span data-ttu-id="02dee-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="02dee-121">2\_x</span></span> | <span data-ttu-id="02dee-122">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="02dee-122">2\_sw</span></span> | <span data-ttu-id="02dee-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="02dee-123">3\_0</span></span> | <span data-ttu-id="02dee-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="02dee-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="02dee-125">xyzw (預設) </span><span class="sxs-lookup"><span data-stu-id="02dee-125">.xyzw (default)</span></span>       | <span data-ttu-id="02dee-126">x</span><span class="sxs-lookup"><span data-stu-id="02dee-126">x</span></span>    | <span data-ttu-id="02dee-127">x</span><span class="sxs-lookup"><span data-stu-id="02dee-127">x</span></span>    | <span data-ttu-id="02dee-128">x</span><span class="sxs-lookup"><span data-stu-id="02dee-128">x</span></span>    | <span data-ttu-id="02dee-129">x</span><span class="sxs-lookup"><span data-stu-id="02dee-129">x</span></span>    | <span data-ttu-id="02dee-130">x</span><span class="sxs-lookup"><span data-stu-id="02dee-130">x</span></span>    | <span data-ttu-id="02dee-131">x</span><span class="sxs-lookup"><span data-stu-id="02dee-131">x</span></span>    | <span data-ttu-id="02dee-132">x</span><span class="sxs-lookup"><span data-stu-id="02dee-132">x</span></span>     | <span data-ttu-id="02dee-133">x</span><span class="sxs-lookup"><span data-stu-id="02dee-133">x</span></span>    | <span data-ttu-id="02dee-134">x</span><span class="sxs-lookup"><span data-stu-id="02dee-134">x</span></span>     |
| <span data-ttu-id="02dee-135">.xyz</span><span class="sxs-lookup"><span data-stu-id="02dee-135">.xyz</span></span>                  | <span data-ttu-id="02dee-136">x</span><span class="sxs-lookup"><span data-stu-id="02dee-136">x</span></span>    | <span data-ttu-id="02dee-137">x</span><span class="sxs-lookup"><span data-stu-id="02dee-137">x</span></span>    | <span data-ttu-id="02dee-138">x</span><span class="sxs-lookup"><span data-stu-id="02dee-138">x</span></span>    | <span data-ttu-id="02dee-139">x</span><span class="sxs-lookup"><span data-stu-id="02dee-139">x</span></span>    | <span data-ttu-id="02dee-140">x</span><span class="sxs-lookup"><span data-stu-id="02dee-140">x</span></span>    | <span data-ttu-id="02dee-141">x</span><span class="sxs-lookup"><span data-stu-id="02dee-141">x</span></span>    | <span data-ttu-id="02dee-142">x</span><span class="sxs-lookup"><span data-stu-id="02dee-142">x</span></span>     | <span data-ttu-id="02dee-143">x</span><span class="sxs-lookup"><span data-stu-id="02dee-143">x</span></span>    | <span data-ttu-id="02dee-144">x</span><span class="sxs-lookup"><span data-stu-id="02dee-144">x</span></span>     |
| <span data-ttu-id="02dee-145">w</span><span class="sxs-lookup"><span data-stu-id="02dee-145">.w</span></span>                    | <span data-ttu-id="02dee-146">x</span><span class="sxs-lookup"><span data-stu-id="02dee-146">x</span></span>    | <span data-ttu-id="02dee-147">x</span><span class="sxs-lookup"><span data-stu-id="02dee-147">x</span></span>    | <span data-ttu-id="02dee-148">x</span><span class="sxs-lookup"><span data-stu-id="02dee-148">x</span></span>    | <span data-ttu-id="02dee-149">x</span><span class="sxs-lookup"><span data-stu-id="02dee-149">x</span></span>    | <span data-ttu-id="02dee-150">x</span><span class="sxs-lookup"><span data-stu-id="02dee-150">x</span></span>    | <span data-ttu-id="02dee-151">x</span><span class="sxs-lookup"><span data-stu-id="02dee-151">x</span></span>    | <span data-ttu-id="02dee-152">x</span><span class="sxs-lookup"><span data-stu-id="02dee-152">x</span></span>     | <span data-ttu-id="02dee-153">x</span><span class="sxs-lookup"><span data-stu-id="02dee-153">x</span></span>    | <span data-ttu-id="02dee-154">x</span><span class="sxs-lookup"><span data-stu-id="02dee-154">x</span></span>     |
| <span data-ttu-id="02dee-155">任意遮罩</span><span class="sxs-lookup"><span data-stu-id="02dee-155">arbitrary mask</span></span>        |      |      |      | <span data-ttu-id="02dee-156">x</span><span class="sxs-lookup"><span data-stu-id="02dee-156">x</span></span>    | <span data-ttu-id="02dee-157">x</span><span class="sxs-lookup"><span data-stu-id="02dee-157">x</span></span>    | <span data-ttu-id="02dee-158">x</span><span class="sxs-lookup"><span data-stu-id="02dee-158">x</span></span>    | <span data-ttu-id="02dee-159">x</span><span class="sxs-lookup"><span data-stu-id="02dee-159">x</span></span>     | <span data-ttu-id="02dee-160">x</span><span class="sxs-lookup"><span data-stu-id="02dee-160">x</span></span>    | <span data-ttu-id="02dee-161">x</span><span class="sxs-lookup"><span data-stu-id="02dee-161">x</span></span>     |



 

<span data-ttu-id="02dee-162">任意的遮罩可讓任何一組通道合併以產生遮罩。</span><span class="sxs-lookup"><span data-stu-id="02dee-162">The arbitrary mask allows any set of channels to be combined to produce a mask.</span></span> <span data-ttu-id="02dee-163">通道必須列在 order r、g、b 和 a-例如 rba，這會更新目的地的紅色、藍色和 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="02dee-163">The channels must be listed in the order r, g, b, a - for example, register.rba, which updates the red, blue, and alpha channels of the destination.</span></span> <span data-ttu-id="02dee-164">您可以在第1版或更高版本中取得任意的遮罩 \_ 。</span><span class="sxs-lookup"><span data-stu-id="02dee-164">The arbitrary mask is available in version 1\_4 or higher.</span></span>

<span data-ttu-id="02dee-165">如果未指定目的地寫入遮罩，目的地寫入遮罩會預設為 rgba 案例。</span><span class="sxs-lookup"><span data-stu-id="02dee-165">If no destination write mask is specified, the destination write mask defaults to the rgba case.</span></span> <span data-ttu-id="02dee-166">換句話說，會更新目的地暫存器中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="02dee-166">In other words, all channels in the destination register are updated.</span></span>

<span data-ttu-id="02dee-167">針對 1 \_ 0 到 1 3 的版本 \_ ， [dp3-ps](dp3---ps.md) dp3 算術指令只能使用 rgb 或 rgba 輸出寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="02dee-167">For versions 1\_0 to 1\_3, the [dp3 - ps](dp3---ps.md) dp3 arithmetic instruction can use only the .rgb or .rgba output write masks.</span></span>

<span data-ttu-id="02dee-168">目的地暫存器寫入遮罩僅支援算數運算。</span><span class="sxs-lookup"><span data-stu-id="02dee-168">Destination register write masks are supported for arithmetic operations only.</span></span> <span data-ttu-id="02dee-169">它們不能用於紋理定址指示，除了第1版的 \_ 指令、 [texcrd-ps](texcrd---ps.md) 和 [texld-ps \_ 2 \_ 0 和更新](texld---ps-2-0.md)版本之外。</span><span class="sxs-lookup"><span data-stu-id="02dee-169">They cannot be used on texture addressing instructions, with the exception of the version 1\_4 instructions, [texcrd - ps](texcrd---ps.md) and [texld - ps\_2\_0 and up](texld---ps-2-0.md).</span></span>

<span data-ttu-id="02dee-170">預設值是寫入全部四個色彩通道。</span><span class="sxs-lookup"><span data-stu-id="02dee-170">The default is to write all four color channels.</span></span>


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



<span data-ttu-id="02dee-171">Alpha 寫入遮罩也稱為純量寫入遮罩，因為它使用純量管線。</span><span class="sxs-lookup"><span data-stu-id="02dee-171">The alpha write mask is also referred to as the scalar write mask, because it uses the scalar pipeline.</span></span>


```
add r0.a, t1, v1
```



<span data-ttu-id="02dee-172">因此，此指示會將 t1 的 Alpha 元件總和和 v1 的 Alpha 元件，有效地放入 r0 中。</span><span class="sxs-lookup"><span data-stu-id="02dee-172">So this instruction effectively puts the sum of the alpha component of t1 and the alpha component of v1 into r0.a.</span></span>

<span data-ttu-id="02dee-173">色彩寫入遮罩是用來控制對色彩通道的寫入。</span><span class="sxs-lookup"><span data-stu-id="02dee-173">The color write mask is used to control writing to the color channels.</span></span>


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



<span data-ttu-id="02dee-174">在第1版中 \_ ，只要遮罩的順序為 r、g、b、a，就可以將目的地寫入遮罩用於任何組合中。</span><span class="sxs-lookup"><span data-stu-id="02dee-174">For version 1\_4, destination write masks can be used in any combination as long as the masks are ordered r,g,b,a.</span></span>


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



<span data-ttu-id="02dee-175">共同發行的指令允許同時發出兩個可能不同的指令。</span><span class="sxs-lookup"><span data-stu-id="02dee-175">A co-issued instruction allows two potentially different instructions to be issued simultaneously.</span></span> <span data-ttu-id="02dee-176">這可透過執行 Alpha 管線和 RGB 管線中的指示來完成。</span><span class="sxs-lookup"><span data-stu-id="02dee-176">This is accomplished by executing the instructions in the alpha pipeline and the RGB pipeline.</span></span>


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



<span data-ttu-id="02dee-177">以這種方式配對指示的優點是，它可讓您以平行方式在向量和純量管線中執行不同的作業。</span><span class="sxs-lookup"><span data-stu-id="02dee-177">The advantage of pairing instructions this way is that it allows different operations to be performed in the vector and scalar pipeline in parallel.</span></span>

<span data-ttu-id="02dee-178">這些頂點著色器輸出暫存器會限制為下列寫入遮罩：</span><span class="sxs-lookup"><span data-stu-id="02dee-178">These vertex shader output registers are restricted to the following write masks:</span></span>



| <span data-ttu-id="02dee-179">註冊類型</span><span class="sxs-lookup"><span data-stu-id="02dee-179">Register Type</span></span> | <span data-ttu-id="02dee-180">必要的寫入遮罩</span><span class="sxs-lookup"><span data-stu-id="02dee-180">Required Write Mask</span></span>                                              |
|---------------|------------------------------------------------------------------|
| <span data-ttu-id="02dee-181">oFog</span><span class="sxs-lookup"><span data-stu-id="02dee-181">oFog</span></span>          | <span data-ttu-id="02dee-182">此純量暫存器不允許明確的寫入遮罩</span><span class="sxs-lookup"><span data-stu-id="02dee-182">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="02dee-183">選擇</span><span class="sxs-lookup"><span data-stu-id="02dee-183">oPts</span></span>          | <span data-ttu-id="02dee-184">此純量暫存器不允許明確的寫入遮罩</span><span class="sxs-lookup"><span data-stu-id="02dee-184">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="02dee-185">oPos</span><span class="sxs-lookup"><span data-stu-id="02dee-185">oPos</span></span>          | <span data-ttu-id="02dee-186">xyzw (預設值) </span><span class="sxs-lookup"><span data-stu-id="02dee-186">.xyzw(which is the default)</span></span>                                      |
| <span data-ttu-id="02dee-187">oT\#</span><span class="sxs-lookup"><span data-stu-id="02dee-187">oT\#</span></span>          | <span data-ttu-id="02dee-188">合併遮罩：. x. \| \| \| xyzw (是預設) </span><span class="sxs-lookup"><span data-stu-id="02dee-188">combined mask: .x \| .xy \| .xyz \| .xyzw (which is the default)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="02dee-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="02dee-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02dee-190">圖元著色器暫存器修飾詞</span><span class="sxs-lookup"><span data-stu-id="02dee-190">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




