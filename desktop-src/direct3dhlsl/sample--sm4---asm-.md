---
title: '範例 (sm4-asm) '
description: '使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。 |範例 (sm4-asm) '
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945937"
---
# <a name="sample-sm4---asm"></a><span data-ttu-id="97c47-104">範例 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="97c47-104">sample (sm4 - asm)</span></span>

<span data-ttu-id="97c47-105">使用指定之取樣器所識別的指定位址和篩選模式，從指定的專案/材質取樣資料。</span><span class="sxs-lookup"><span data-stu-id="97c47-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="97c47-106">範例 \[ \_ aoffimmi (u，v，w) \] dest \[ . mask \] ，srcAddress \[ . swizzle \] ，srcResource， \[ swizzle \] ，srcSampler</span><span class="sxs-lookup"><span data-stu-id="97c47-106">sample\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="97c47-107">項目</span><span class="sxs-lookup"><span data-stu-id="97c47-107">Item</span></span>                                                                                                               | <span data-ttu-id="97c47-108">描述</span><span class="sxs-lookup"><span data-stu-id="97c47-108">Description</span></span>                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97c47-109"><span id="dest"></span><span id="DEST"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="97c47-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="97c47-110">\[在 \] 操作結果的位址中。</span><span class="sxs-lookup"><span data-stu-id="97c47-110">\[in\] The address of the result of the operation.</span></span><br/>                                      |
| <span data-ttu-id="97c47-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="97c47-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="97c47-112">\[在 \] 一組材質座標中。</span><span class="sxs-lookup"><span data-stu-id="97c47-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="97c47-113">如需詳細資訊，請參閱「 **備註** 」一節。</span><span class="sxs-lookup"><span data-stu-id="97c47-113">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="97c47-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="97c47-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="97c47-115">\[在材質暫存器中 \] 。</span><span class="sxs-lookup"><span data-stu-id="97c47-115">\[in\] A texture register.</span></span> <span data-ttu-id="97c47-116">如需詳細資訊，請參閱「 **備註** 」一節。</span><span class="sxs-lookup"><span data-stu-id="97c47-116">For more information, see the **Remarks** section.</span></span><br/>           |
| <span data-ttu-id="97c47-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="97c47-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="97c47-118">\[在 \] 取樣器註冊中。</span><span class="sxs-lookup"><span data-stu-id="97c47-118">\[in\] A sampler register.</span></span> <span data-ttu-id="97c47-119">如需詳細資訊，請參閱「 **備註** 」一節。</span><span class="sxs-lookup"><span data-stu-id="97c47-119">For more information, see the **Remarks** section.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="97c47-120">備註</span><span class="sxs-lookup"><span data-stu-id="97c47-120">Remarks</span></span>

<span data-ttu-id="97c47-121">來源資料可能來自于緩衝區以外的任何資源類型。</span><span class="sxs-lookup"><span data-stu-id="97c47-121">The source data may come from any Resource Type, other than Buffers.</span></span>

<span data-ttu-id="97c47-122">*srcAddress* 會提供執行範例所需的材質座標集合，做為參考材質中正規化空間的浮點值。</span><span class="sxs-lookup"><span data-stu-id="97c47-122">*srcAddress* provides the set of texture coordinates needed to perform the sample, as floating point values referencing normalized space in the texture.</span></span> <span data-ttu-id="97c47-123">位址包裝模式 (wrap/鏡像/夾具/框線等。 ) 會套用 \[ 至 0 ... 1 範圍以外的材質座標 \] ，從取樣器狀態 (s \#) ，然後在任何位址位移套用至材質座標之後套用。</span><span class="sxs-lookup"><span data-stu-id="97c47-123">Address wrapping modes (wrap/mirror/clamp/border etc.) are applied for texture coordinates outside \[0...1\] range, taken from the sampler state (s\#), and applied after any address offset is applied to texture coordinates.</span></span>

<span data-ttu-id="97c47-124">*srcResource* 是 (t) 的材質暫存器 \# 。</span><span class="sxs-lookup"><span data-stu-id="97c47-124">*srcResource* is a texture register (t\#).</span></span> <span data-ttu-id="97c47-125">這只是材質的預留位置，包括所取樣資源的傳回資料類型。</span><span class="sxs-lookup"><span data-stu-id="97c47-125">This is simply a placeholder for a texture, including the return data type of the resource being sampled.</span></span> <span data-ttu-id="97c47-126">所有這些資訊都是在著色器前序中宣告的。</span><span class="sxs-lookup"><span data-stu-id="97c47-126">All of this information is declared in the Shader preamble.</span></span> <span data-ttu-id="97c47-127">實際要取樣的資源會系結至 t) 位置 (外部的著色器 \# \# 。</span><span class="sxs-lookup"><span data-stu-id="97c47-127">The actual resource to be sampled is bound to the Shader externally at slot \# (for t\#).</span></span>

<span data-ttu-id="97c47-128">*srcSampler* 是 (s) 的取樣器註冊。</span><span class="sxs-lookup"><span data-stu-id="97c47-128">*srcSampler* is a sampler register (s).</span></span> <span data-ttu-id="97c47-129">這只是篩選控制項集合的預留位置，例如 point 和線性、mipmap 和位址換行控制項。</span><span class="sxs-lookup"><span data-stu-id="97c47-129">This is simply a placeholder for a collection of filtering controls such as point vs. linear, mipmapping and address wrapping controls.</span></span>

<span data-ttu-id="97c47-130">執行取樣的硬體所需的一組資訊，會分割成兩個垂直片段。</span><span class="sxs-lookup"><span data-stu-id="97c47-130">The set of information required for the hardware to perform sampling is split into two orthogonal pieces.</span></span> <span data-ttu-id="97c47-131">首先，材質暫存器會提供源資料類型資訊，例如，材質是否包含 SRGB 資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97c47-131">First, the texture register provides source data type information including, for example, information about whether the texture contains SRGB data.</span></span> <span data-ttu-id="97c47-132">它也會參考實際取樣的記憶體。</span><span class="sxs-lookup"><span data-stu-id="97c47-132">It also references the actual memory being sampled.</span></span> <span data-ttu-id="97c47-133">其次，取樣器註冊會定義要套用的篩選模式。</span><span class="sxs-lookup"><span data-stu-id="97c47-133">Second, the sampler register defines the filtering mode to apply.</span></span>

### <a name="array-resources"></a><span data-ttu-id="97c47-134">陣列資源</span><span class="sxs-lookup"><span data-stu-id="97c47-134">Array Resources</span></span>

<span data-ttu-id="97c47-135">針對 Texture1D 陣列， *srcAddress* g 元件 (POS swizzle) 選取要從中提取的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="97c47-135">For Texture1D Arrays, the *srcAddress* g component (POS-swizzle) selects which Array Slice to fetch from.</span></span> <span data-ttu-id="97c47-136">這一律會被視為縮放的浮點值，而不是標準材質座標的正規化空間，而是在值上套用四捨五入至最接近的值，接著是套用至可用 BufferArray 範圍的值。</span><span class="sxs-lookup"><span data-stu-id="97c47-136">This is always treated as a scaled float value, rather than the normalized space for standard texture coordinates, and a round-to-nearest even is applied on the value, followed by a clamp to the available BufferArray range.</span></span>

<span data-ttu-id="97c47-137">針對 Texture2D 陣列， *srcAddress* b 元件 (POS-swizzle) 選取要從中提取的陣列配量，否則使用 Texture1D 陣列所述的相同語義。</span><span class="sxs-lookup"><span data-stu-id="97c47-137">For Texture2D Arrays, the *srcAddress* b component (POS-swizzle) selects which Array Slice to fetch from, otherwise using the same semantics described for Texture1D Arrays .</span></span>

### <a name="address-offset"></a><span data-ttu-id="97c47-138">位址位移</span><span class="sxs-lookup"><span data-stu-id="97c47-138">Address Offset</span></span>

<span data-ttu-id="97c47-139">選擇性的 \[ \_ aoffimmi (u，v，w) \] 尾碼 (以立即整數的位址位移) 表示樣本的材質座標是以一組提供的立即材質空間整數常數值來位移。</span><span class="sxs-lookup"><span data-stu-id="97c47-139">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the sample are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="97c47-140">常值是一組4位2的補數數位，具有整數範圍 \[ -8，7 \] 。</span><span class="sxs-lookup"><span data-stu-id="97c47-140">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="97c47-141">此修飾詞會針對所有資源（包括 Texture1D/2D 陣列和 Texture3D）定義，但不會針對 TextureCube 定義。</span><span class="sxs-lookup"><span data-stu-id="97c47-141">This modifier is defined for all Resources, including Texture1D/2D Arrays and Texture3D, but it is undefined for TextureCube.</span></span>

<span data-ttu-id="97c47-142">硬體可以利用立即的知識，讓您透過一組範例指令來執行有關常見位置的一些材質使用量。</span><span class="sxs-lookup"><span data-stu-id="97c47-142">Hardware can take advantage of immediate knowledge that a traversal over some footprint of texels about a common location is being performed by a set of sample instructions.</span></span> <span data-ttu-id="97c47-143">這可以使用 \_ aoffimmi (u、v、w) 來傳達。</span><span class="sxs-lookup"><span data-stu-id="97c47-143">This can be conveyed using \_aoffimmi(u,v,w).</span></span>

<span data-ttu-id="97c47-144">位移會新增至材質座標（在材質空間中），相對於每個要存取的 miplevel。</span><span class="sxs-lookup"><span data-stu-id="97c47-144">The offsets are added to the texture coordinates, in texel space, relative to each miplevel being accessed.</span></span> <span data-ttu-id="97c47-145">因此，即使材質座標是以正規化浮點數的形式提供，位移也會套用材質空間的整數位移。</span><span class="sxs-lookup"><span data-stu-id="97c47-145">So even though texture coordinates are provided as normalized float values, the offset applies a texel-space integer offset.</span></span>

<span data-ttu-id="97c47-146">Texture1D/2D 陣列的陣列軸並不會套用位址位移。</span><span class="sxs-lookup"><span data-stu-id="97c47-146">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="97c47-147">\_aoffimmi v，會忽略 Texture1Ds 的 w 元件。</span><span class="sxs-lookup"><span data-stu-id="97c47-147">\_aoffimmi v,w components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="97c47-148">\_Texture2Ds 會忽略 aoffimmi w 元件。</span><span class="sxs-lookup"><span data-stu-id="97c47-148">\_aoffimmi w component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="97c47-149">位址換行模式 (wrap/鏡像/夾具/框線等。從取樣器狀態 )  (s \#) 會在任何位址位移套用至材質座標之後套用。</span><span class="sxs-lookup"><span data-stu-id="97c47-149">Address wrapping modes (wrap/mirror/clamp/border etc.) from the sampler state (s\#) are applied after any address offset is applied to texture coordinates.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="97c47-150">傳回型別控制項</span><span class="sxs-lookup"><span data-stu-id="97c47-150">Return Type Control</span></span>

<span data-ttu-id="97c47-151">範例所傳回的資料格式是由 (DXGI 格式的資源格式所決定，) 系 \_ 結 \* 至 (t) 的 *srcResource* 參數 \# 。</span><span class="sxs-lookup"><span data-stu-id="97c47-151">The data format returned by the sample to the destination register is determined by the resource format (DXGI\_FORMAT\*) bound to the *srcResource* parameter (t\#).</span></span> <span data-ttu-id="97c47-152">例如，如果指定的 t 系結于 \# 格式為 DXGI \_ 格式 \_ A8B8G8R8 \_ UNORM SRGB 的資源 \_ ，則取樣作業會將取樣的材質從 gamma 2.0 轉換為1.0，套用篩選，並將結果寫入至目的地暫存器做為範圍 0 ..1 中的浮點值 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="97c47-152">For example, if the specified t\# was bound with a resource with format DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB, then the sampling operation will convert sampled texels from gamma 2.0 to 1.0, apply filtering, and the result will written to the destination register as floating point values in the range \[0..1\].</span></span>

<span data-ttu-id="97c47-153">傳回的值為4向量 (以及格式) 不存在的元件的格式特定預設值。</span><span class="sxs-lookup"><span data-stu-id="97c47-153">Returned values are 4-vectors (with format-specific defaults for components not present in the format).</span></span> <span data-ttu-id="97c47-154">*SrcResource* 上的 swizzle 會決定如何 swizzle 從紋理取樣/篩選傳回的4個元件結果，在此之後，在 *目標* 上的遮罩會決定 *目的地* 中的哪些元件會更新。</span><span class="sxs-lookup"><span data-stu-id="97c47-154">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture sample/filter, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="97c47-155">當 **範例** 將32位的 float 值讀取至32位的暫存器中，並使用點取樣 (沒有篩選) ，它可能會或可能不會排清 denormal 值，否則不會修改數位。</span><span class="sxs-lookup"><span data-stu-id="97c47-155">When **sample** reads a 32-bit float value into a 32-bit register, with point sampling (no filtering), it may or may not flush denormal values, but otherwise numbers are unmodified.</span></span> <span data-ttu-id="97c47-156">如果點取樣 denormal 值的不確定性是應用程式的問題，請使用 [ld](ld--sm4---asm-.md) 指令，以保證32位的 float 值會以未修改的方式讀取。</span><span class="sxs-lookup"><span data-stu-id="97c47-156">If the uncertainty with point sampling denormal values is an issue for an application,use the [ld](ld--sm4---asm-.md) instruction, which guarantees that 32-bit float values are read unmodified.</span></span>

### <a name="lod-calculation"></a><span data-ttu-id="97c47-157">」 LOD 計算</span><span class="sxs-lookup"><span data-stu-id="97c47-157">LOD Calculation</span></span>

<span data-ttu-id="97c47-158">如需有關如何在判斷」 LOD 以進行篩選的過程中計算衍生的詳細資訊，請參閱 [deriv \_ rtx](deriv-rtx--sm4---asm-.md) 和 [deriv \_ rty](deriv-rty--sm4---asm-.md)。</span><span class="sxs-lookup"><span data-stu-id="97c47-158">For details on how derivatives are calculated in the process of determining LOD for filtering, see [deriv\_rtx](deriv-rtx--sm4---asm-.md) and [deriv\_rty](deriv-rty--sm4---asm-.md).</span></span> <span data-ttu-id="97c47-159">**範例指令範例** 會使用 **deriv** 著色器指令所使用的相同定義，以隱含方式計算紋理座標上的衍生。</span><span class="sxs-lookup"><span data-stu-id="97c47-159">The **sample** instruction implicitly computes derivatives on the texture coordinates using the same definition that the **deriv** Shader instructions use.</span></span> <span data-ttu-id="97c47-160">這並不適用于 [範例 \_ l](sample-l--sm4---asm-.md) 或 [範例 \_ d](sample-d--sm4---asm-.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="97c47-160">This does not apply to [sample\_l](sample-l--sm4---asm-.md) or [sample\_d](sample-d--sm4---asm-.md) instructions.</span></span> <span data-ttu-id="97c47-161">這些指示會直接由應用程式提供」 LOD 或衍生。</span><span class="sxs-lookup"><span data-stu-id="97c47-161">For those instructions, LOD or derivatives are provided directly by the application.</span></span>

<span data-ttu-id="97c47-162">針對 **範例** 指令，執行程式可以選擇在2x2 戳記中的所有4個圖元之間共用相同的」 lod 計算 (但沒有較大的區域) ，或執行每個圖元的」 lod 計算。</span><span class="sxs-lookup"><span data-stu-id="97c47-162">For the **sample** instruction, implementations can choose to share the same LOD calculation across all 4 pixels in a 2x2 stamp (but no larger area), or perform per-pixel LOD calculations.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="97c47-163">其他詳細資料</span><span class="sxs-lookup"><span data-stu-id="97c47-163">Miscellaneous Details</span></span>

<span data-ttu-id="97c47-164">針對 Buffer & Texture1D，會忽略 *srcAddress* (POS swizzle) 的 gba 元件。</span><span class="sxs-lookup"><span data-stu-id="97c47-164">For Buffer & Texture1D, *srcAddress* .gba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="97c47-165">若為 Texture1D 陣列，則會忽略 *srcAddress* (POS-swizzle) 的元件。</span><span class="sxs-lookup"><span data-stu-id="97c47-165">For Texture1D Arrays, *srcAddress* .ba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="97c47-166">若為 Texture2Ds，則會忽略 *srcAddress* (POS-swizzle) 的元件。</span><span class="sxs-lookup"><span data-stu-id="97c47-166">For Texture2Ds, *srcAddress* .a component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="97c47-167">從未系結任何專案的輸入位置提取，會針對所有元件傳回0。</span><span class="sxs-lookup"><span data-stu-id="97c47-167">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="97c47-168">限制</span><span class="sxs-lookup"><span data-stu-id="97c47-168">Restrictions</span></span>

-   <span data-ttu-id="97c47-169">*srcResource* 必須是 t \# 註冊。</span><span class="sxs-lookup"><span data-stu-id="97c47-169">*srcResource* must be a t\# register.</span></span> <span data-ttu-id="97c47-170">*srcResource* 不能是無法系結至 t 註冊的 ConstantBuffer \# 。</span><span class="sxs-lookup"><span data-stu-id="97c47-170">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="97c47-171">*srcSampler* 必須是 s \# 註冊。</span><span class="sxs-lookup"><span data-stu-id="97c47-171">*srcSampler* must be an s\# register.</span></span>
-   <span data-ttu-id="97c47-172">不允許 *srcResource* 或 *srcSampler* 的相對定址。</span><span class="sxs-lookup"><span data-stu-id="97c47-172">Relative addressing on *srcResource* or *srcSampler* is not permitted.</span></span>
-   <span data-ttu-id="97c47-173">*srcAddress* 必須是 temp (r \# /X \#) 、constantBuffer (cb \#) 、輸入 (v \#) register 或立即值 (s) 。</span><span class="sxs-lookup"><span data-stu-id="97c47-173">*srcAddress* must be a temp (r\#/x\#), constantBuffer (cb\#), input (v\#) register or immediate value(s).</span></span>
-   <span data-ttu-id="97c47-174">*dest* 必須是 temp (r \# /x \#) 或 output (o \* \#) register。</span><span class="sxs-lookup"><span data-stu-id="97c47-174">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>
-   <span data-ttu-id="97c47-175">\_TextureCubes 不允許 aoffimmi (u，v，w) 。</span><span class="sxs-lookup"><span data-stu-id="97c47-175">\_aoffimmi(u,v,w) is not permitted for TextureCubes.</span></span>

<span data-ttu-id="97c47-176">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="97c47-176">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="97c47-177">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="97c47-177">Vertex Shader</span></span> | <span data-ttu-id="97c47-178">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="97c47-178">Geometry Shader</span></span> | <span data-ttu-id="97c47-179">像素著色器</span><span class="sxs-lookup"><span data-stu-id="97c47-179">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="97c47-180">x</span><span class="sxs-lookup"><span data-stu-id="97c47-180">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="97c47-181">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="97c47-181">Minimum Shader Model</span></span>

<span data-ttu-id="97c47-182">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="97c47-182">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="97c47-183">著色器模型</span><span class="sxs-lookup"><span data-stu-id="97c47-183">Shader Model</span></span>                                              | <span data-ttu-id="97c47-184">支援</span><span class="sxs-lookup"><span data-stu-id="97c47-184">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="97c47-185">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="97c47-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="97c47-186">是</span><span class="sxs-lookup"><span data-stu-id="97c47-186">yes</span></span>       |
| [<span data-ttu-id="97c47-187">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="97c47-187">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="97c47-188">是</span><span class="sxs-lookup"><span data-stu-id="97c47-188">yes</span></span>       |
| [<span data-ttu-id="97c47-189">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="97c47-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="97c47-190">是</span><span class="sxs-lookup"><span data-stu-id="97c47-190">yes</span></span>       |
| [<span data-ttu-id="97c47-191">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="97c47-191">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="97c47-192">不可以</span><span class="sxs-lookup"><span data-stu-id="97c47-192">no</span></span>        |
| [<span data-ttu-id="97c47-193">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="97c47-193">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="97c47-194">不可以</span><span class="sxs-lookup"><span data-stu-id="97c47-194">no</span></span>        |
| [<span data-ttu-id="97c47-195">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="97c47-195">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="97c47-196">不可以</span><span class="sxs-lookup"><span data-stu-id="97c47-196">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="97c47-197">相關主題</span><span class="sxs-lookup"><span data-stu-id="97c47-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97c47-198">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="97c47-198">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





