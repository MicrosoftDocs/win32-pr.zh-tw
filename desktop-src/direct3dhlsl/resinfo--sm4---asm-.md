---
title: 'resinfo (sm4-asm) '
description: 查詢指定輸入資源的維度。
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373766"
---
# <a name="resinfo-sm4---asm"></a><span data-ttu-id="3336d-103">resinfo (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="3336d-103">resinfo (sm4 - asm)</span></span>

<span data-ttu-id="3336d-104">查詢指定輸入資源的維度。</span><span class="sxs-lookup"><span data-stu-id="3336d-104">Query the dimensions of a given input resource.</span></span>



| <span data-ttu-id="3336d-105">resinfo \[ \_ uint </span><span class="sxs-lookup"><span data-stu-id="3336d-105">resinfo\[\_uint</span></span>\|<span data-ttu-id="3336d-106">\_rcpFloat \] dest \[ . mask \] ，srcMipLevel. Select \_ component，srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3336d-106">\_rcpFloat\] dest\[.mask\], srcMipLevel.select\_component, srcResource\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3336d-107">項目</span><span class="sxs-lookup"><span data-stu-id="3336d-107">Item</span></span>                                                                                                               | <span data-ttu-id="3336d-108">描述</span><span class="sxs-lookup"><span data-stu-id="3336d-108">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3336d-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="3336d-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="3336d-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="3336d-110">\[in\] The address of the result of the operation.</span></span><br/>                             |
| <span data-ttu-id="3336d-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span><span class="sxs-lookup"><span data-stu-id="3336d-111"><span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*</span></span><br/> | <span data-ttu-id="3336d-112">\[在 \] mip 層級中。</span><span class="sxs-lookup"><span data-stu-id="3336d-112">\[in\] The mip level.</span></span><br/>                                                          |
| <span data-ttu-id="3336d-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="3336d-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="3336d-114">\[在要 \] \# 查詢維度的 t 或 u \# 輸入材質中。</span><span class="sxs-lookup"><span data-stu-id="3336d-114">\[in\] A t\# or u\# input texture for which the dimensions are being queried.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3336d-115">備註</span><span class="sxs-lookup"><span data-stu-id="3336d-115">Remarks</span></span>

<span data-ttu-id="3336d-116">*srcMipLevel* 會讀取為不帶正負號的整數純量，因此來源暫存器需要單一元件選取器（如果它不是純量立即值）。</span><span class="sxs-lookup"><span data-stu-id="3336d-116">*srcMipLevel* is read as an unsigned integer scalar so a single component selector is required for the source register, if it is not a scalar immediate value.</span></span>

<span data-ttu-id="3336d-117">*dest* 會接收 \[ \] 寫入遮罩所選取的寬度、高度、深度或陣列大小，總計-mip-count。</span><span class="sxs-lookup"><span data-stu-id="3336d-117">*dest* receives \[width, height, depth or array size, total-mip-count\], selected by the write mask.</span></span>

<span data-ttu-id="3336d-118">傳回的寬度、高度和深度值適用于 *srcMipLevel* 參數所選取的 mip 層級，而且是材質數目，與材質資料大小無關。</span><span class="sxs-lookup"><span data-stu-id="3336d-118">The returned width, height and depth values are for the mip-level selected by the *srcMipLevel* parameter, and are in number of texels, independent of texel data size.</span></span> <span data-ttu-id="3336d-119">針對高取樣資源 (texture2D \[ 陣列 \] MS \#) ，寬度和高度也會在材質中傳回，而非範例。</span><span class="sxs-lookup"><span data-stu-id="3336d-119">For multisample resources (texture2D\[Array\]MS\#), width and height are also returned in texels, not samples.</span></span>

<span data-ttu-id="3336d-120">在 *dest* 中傳回的 mip 計數總計未受到 *srcMipLevel* 參數的影響。</span><span class="sxs-lookup"><span data-stu-id="3336d-120">The total mip count returned in *dest.w* is unaffected by the *srcMipLevel* parameter.</span></span>

<span data-ttu-id="3336d-121">針對 UAVs (u \#) ，mip 層級的數目一律為1。</span><span class="sxs-lookup"><span data-stu-id="3336d-121">For UAVs (u\#), the number of mip levels is always 1.</span></span>

<span data-ttu-id="3336d-122">此指示的所有層面都是以 t/u 系結資源檢視的特性為基礎 \# \# ，而不是基礎基底資源。</span><span class="sxs-lookup"><span data-stu-id="3336d-122">All aspects of this instruction are based on the characteristics of the resource view bound at the t\#/u\#, not the underlying base resource.</span></span>

<span data-ttu-id="3336d-123">除非使用 uint 修飾詞，否則傳回的值都是浮點數， \_ 在這種情況下，傳回的值全都是整數。</span><span class="sxs-lookup"><span data-stu-id="3336d-123">Returned values are all floating point, unless the \_uint modifier is used, in which case the returned values are all integers.</span></span> <span data-ttu-id="3336d-124">如果 \_ 使用 rcpFloat 修飾詞，所有傳回的值都是浮點數，而寬度、高度和深度會傳回為 reciprocals (1.0 f/寬度、1.0 f/高度、1.0 f/深度) ，包括如果寬度/高度/深度為0（從超出範圍 *srcMipLevel* 行為）。</span><span class="sxs-lookup"><span data-stu-id="3336d-124">If the \_rcpFloat modifier is used, all returned values are floating point, and the width, height and depth are returned as reciprocals (1.0f/width, 1.0f/height, 1.0f/depth), including INF if width/height/depth are 0 from out-of-range *srcMipLevel* behavior.</span></span> <span data-ttu-id="3336d-125">\_RcpFloat 修飾詞只適用于 width、height 和 depth 傳回的值，而且不會套用至設定為0且不會傳回的值，也不會套用至陣列大小傳回。</span><span class="sxs-lookup"><span data-stu-id="3336d-125">The \_rcpFloat modifier only applies to width, height, and depth returned values and does not apply to values that are set to 0 and thus not returned, and also does not apply to array size returns.</span></span>

<span data-ttu-id="3336d-126">*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。</span><span class="sxs-lookup"><span data-stu-id="3336d-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="3336d-127">如果 *srcResource* 是 Texture1D，則會在 *dest* 中傳回 width，而 *dest. yz* 會設定為0。</span><span class="sxs-lookup"><span data-stu-id="3336d-127">If *srcResource* is a Texture1D, then width is returned in *dest.x*, and *dest.yz* are set to 0.</span></span>

<span data-ttu-id="3336d-128">如果 *srcResource* 是 Texture1DArray，則會在 *dest* 中傳回 width，陣列大小會在 *dest* 中傳回，而 *dest* 會設定為0。</span><span class="sxs-lookup"><span data-stu-id="3336d-128">If *srcResource* is a Texture1DArray, then width is returned in *dest.x*, the array size is returned in *dest.y*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="3336d-129">如果 *srcResource* 是 Texture2D，則會在 *dest* 中傳回寬度和高度，並將 *dest* 設定為0。</span><span class="sxs-lookup"><span data-stu-id="3336d-129">If *srcResource* is a Texture2D, then width and height are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="3336d-130">如果 *srcResource* 是 Texture2DArray，則寬度和高度會在 *dest* 中傳回，而陣列大小則會在 *目的地. z* 中傳回。</span><span class="sxs-lookup"><span data-stu-id="3336d-130">If *srcResource* is a Texture2DArray, then width and height are returned in *dest.xy*, and the array size is returned in *dest.z*.</span></span>

<span data-ttu-id="3336d-131">如果 *srcResource* 是 Texture3D，則會在 *dest.xyz* 中傳回寬度、高度和深度。</span><span class="sxs-lookup"><span data-stu-id="3336d-131">If *srcResource* is a Texture3D, then width, height and depth are returned in *dest.xyz*.</span></span>

<span data-ttu-id="3336d-132">如果 *srcResource* 是 TextureCube，則個別 cube 臉部維度的寬度和高度會在 *dest* 中傳回，而 *目的地. z* 會設定為0。</span><span class="sxs-lookup"><span data-stu-id="3336d-132">If *srcResource* is a TextureCube, then the width and height of the individual cube face dimensions are returned in *dest.xy*, and *dest.z* is set to 0.</span></span>

<span data-ttu-id="3336d-133">如果 *srcResource* 是 TextureCubeArray，則個別 cube 臉部維度的寬度和高度會在 *dest* 中傳回。</span><span class="sxs-lookup"><span data-stu-id="3336d-133">If *srcResource* is a TextureCubeArray, then the width and height the individual cube face dimensions are returned in *dest.xy*.</span></span> <span data-ttu-id="3336d-134">*目的地 z* 設定為未定義的值。</span><span class="sxs-lookup"><span data-stu-id="3336d-134">*dest.z* is set to an undefined value.</span></span>

<span data-ttu-id="3336d-135">如果在 *srcResource* 上指定了每個資源的 mip 夾具，resinfo 一律會傳回 mip 計數的視圖中的 mipmap 總數（不論是否有此夾具）。</span><span class="sxs-lookup"><span data-stu-id="3336d-135">If the a per-resource mip clamp has been specified on *srcResource*, resinfo always returns the total number of mipmaps in the view for the mip count, regardless of the clamp.</span></span> <span data-ttu-id="3336d-136">但是，如果指定之 miplevel 的維度是由 resinfo 所要求，且 miplevel 已壓制 off (例如，2.2 的夾具表示已將 mips 0 和1壓制關閉) ，則傳回的維度並未定義。</span><span class="sxs-lookup"><span data-stu-id="3336d-136">However, if the dimensions of a given miplevel are requested by resinfo and the miplevel has been clamped off (e.g. a clamp of 2.2 means that mips 0 and 1 have been clamped off), the dimensions returned are undefined.</span></span> <span data-ttu-id="3336d-137">某些實 resinfo 會在 miplevel 超出範圍時，傳回針對指定的超出範圍行為。</span><span class="sxs-lookup"><span data-stu-id="3336d-137">Some implementations will return the out of bounds behavior specified for resinfo when the miplevel is out of range.</span></span> <span data-ttu-id="3336d-138">其他的執行會傳回 mip 的維度，就像尚未壓制。</span><span class="sxs-lookup"><span data-stu-id="3336d-138">Other implementations will return the dimensions of the mip as if it had not been clamped.</span></span>

### <a name="restrictions"></a><span data-ttu-id="3336d-139">限制</span><span class="sxs-lookup"><span data-stu-id="3336d-139">Restrictions</span></span>

-   <span data-ttu-id="3336d-140">*srcResource* 必須是 \# \# 非緩衝區的 t 或 u 暫存器，但卻是材質 \* 。</span><span class="sxs-lookup"><span data-stu-id="3336d-140">*srcResource* must be a t\# or u\# register that is not a Buffer, but is a Texture\*.</span></span>
-   <span data-ttu-id="3336d-141">不允許 *srcResource* 的相對定址。</span><span class="sxs-lookup"><span data-stu-id="3336d-141">Relative addressing of *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="3336d-142">如果 *srcMipLevel* 不是純量立即的，則必須使用單一元件選取器。</span><span class="sxs-lookup"><span data-stu-id="3336d-142">*srcMipLevel* must use a single component selector if it is not a scalar immediate.</span></span>
-   <span data-ttu-id="3336d-143">從 \# 沒有任何系結的 t 或 u 提取，會傳回0（ \# 寬度、高度、深度或 arraysize）和總計 mip 計數。</span><span class="sxs-lookup"><span data-stu-id="3336d-143">Fetching from t\# or u\# that has nothing bound to it returns 0 for width, height, depth or arraysize, and total-mip-count.</span></span> <span data-ttu-id="3336d-144">\_在此情況下，仍會接受 rcpFloat 修飾詞，因此會針對適用的傳回值傳回 INF。</span><span class="sxs-lookup"><span data-stu-id="3336d-144">The \_rcpFloat modifier is still honored in this case, thus returning INF for the applicable returned values.</span></span>
-   <span data-ttu-id="3336d-145">如果 *srcMipLevel* 超出資源中可用 miplevels 數目的範圍，則大小的行為會傳回 (*dest.xyz*) 等同于未系結的 t \# 或 u \# 資源。</span><span class="sxs-lookup"><span data-stu-id="3336d-145">If *srcMipLevel* is out of the range of the available number of miplevels in the resource, the behavior for the size return (*dest.xyz*) is identical to that of an unbound t\# or u\# resource.</span></span> <span data-ttu-id="3336d-146">在此情況下，在 *dest* 中仍會傳回 mip 總計計數。</span><span class="sxs-lookup"><span data-stu-id="3336d-146">The total mip count is still returned in *dest.w* for this case.</span></span>

<span data-ttu-id="3336d-147">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="3336d-147">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3336d-148">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="3336d-148">Vertex Shader</span></span> | <span data-ttu-id="3336d-149">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="3336d-149">Geometry Shader</span></span> | <span data-ttu-id="3336d-150">像素著色器</span><span class="sxs-lookup"><span data-stu-id="3336d-150">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3336d-151">x</span><span class="sxs-lookup"><span data-stu-id="3336d-151">x</span></span>             | <span data-ttu-id="3336d-152">x</span><span class="sxs-lookup"><span data-stu-id="3336d-152">x</span></span>               | <span data-ttu-id="3336d-153">x</span><span class="sxs-lookup"><span data-stu-id="3336d-153">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3336d-154">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3336d-154">Minimum Shader Model</span></span>

<span data-ttu-id="3336d-155">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="3336d-155">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3336d-156">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3336d-156">Shader Model</span></span>                                              | <span data-ttu-id="3336d-157">支援</span><span class="sxs-lookup"><span data-stu-id="3336d-157">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3336d-158">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3336d-158">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3336d-159">是</span><span class="sxs-lookup"><span data-stu-id="3336d-159">yes</span></span>       |
| [<span data-ttu-id="3336d-160">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="3336d-160">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3336d-161">是</span><span class="sxs-lookup"><span data-stu-id="3336d-161">yes</span></span>       |
| [<span data-ttu-id="3336d-162">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="3336d-162">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3336d-163">是</span><span class="sxs-lookup"><span data-stu-id="3336d-163">yes</span></span>       |
| [<span data-ttu-id="3336d-164">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3336d-164">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3336d-165">不可以</span><span class="sxs-lookup"><span data-stu-id="3336d-165">no</span></span>        |
| [<span data-ttu-id="3336d-166">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3336d-166">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3336d-167">不可以</span><span class="sxs-lookup"><span data-stu-id="3336d-167">no</span></span>        |
| [<span data-ttu-id="3336d-168">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3336d-168">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3336d-169">不可以</span><span class="sxs-lookup"><span data-stu-id="3336d-169">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3336d-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="3336d-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3336d-171">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3336d-171">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





