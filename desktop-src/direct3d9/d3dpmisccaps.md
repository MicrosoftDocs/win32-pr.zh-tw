---
description: 其他驅動程式基本功能旗標。
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ace0b9070d158769e22e02a759545b1bf7785
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343133"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="6e865-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="6e865-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="6e865-104">其他驅動程式基本功能旗標。</span><span class="sxs-lookup"><span data-stu-id="6e865-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6e865-105">#定義</span><span class="sxs-lookup"><span data-stu-id="6e865-105">#define</span></span></td>
<td><span data-ttu-id="6e865-106">值</span><span class="sxs-lookup"><span data-stu-id="6e865-106">Value</span></span></td>
<td><span data-ttu-id="6e865-107">描述</span><span class="sxs-lookup"><span data-stu-id="6e865-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="6e865-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="6e865-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="6e865-109">0x00000002L</span></span></td>
<td><span data-ttu-id="6e865-110">裝置可以啟用和停用圖元作業的深度緩衝區修改。</span><span class="sxs-lookup"><span data-stu-id="6e865-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="6e865-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="6e865-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="6e865-112">0x00000010L</span></span></td>
<td><span data-ttu-id="6e865-113">驅動程式不會執行三角形剔除。</span><span class="sxs-lookup"><span data-stu-id="6e865-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="6e865-114">這會對應至 <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> 列舉型別的 D3DCULL_NONE 成員。</span><span class="sxs-lookup"><span data-stu-id="6e865-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="6e865-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="6e865-116">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="6e865-116">0x00000020L</span></span></td>
<td><span data-ttu-id="6e865-117">此驅動程式支援透過 D3DRS_CULLMODE 狀態進行順時針三角形的挑選。</span><span class="sxs-lookup"><span data-stu-id="6e865-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="6e865-118"> (這只適用于三角形基本專案。 ) 此旗標對應至 <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> 列舉型別的 D3DCULL_CW 成員。</span><span class="sxs-lookup"><span data-stu-id="6e865-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="6e865-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="6e865-120">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="6e865-120">0x00000040L</span></span></td>
<td><span data-ttu-id="6e865-121">此驅動程式支援透過 D3DRS_CULLMODE 狀態的逆時針剔除。</span><span class="sxs-lookup"><span data-stu-id="6e865-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="6e865-122"> (這只適用于三角形基本專案。 ) 此旗標對應至 <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> 列舉型別的 D3DCULL_CCW 成員。</span><span class="sxs-lookup"><span data-stu-id="6e865-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="6e865-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="6e865-124">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="6e865-124">0x00000100L</span></span></td>
<td><span data-ttu-id="6e865-125">裝置可透過 D3DRS_COLORWRITEENABLE 狀態，針對轉譯目標色彩緩衝區支援每個通道的寫入。</span><span class="sxs-lookup"><span data-stu-id="6e865-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="6e865-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="6e865-127">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="6e865-127">0x00000200L</span></span></td>
<td><span data-ttu-id="6e865-128">裝置會正確地將大小大於1.0 的縮放點裁剪到使用者定義的裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="6e865-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="6e865-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="6e865-130">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="6e865-130">0x00000200L</span></span></td>
<td><span data-ttu-id="6e865-131">裝置會裁剪轉換後的頂點基本專案。</span><span class="sxs-lookup"><span data-stu-id="6e865-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="6e865-132">指定管線不應進行任何裁剪時的 D3DUSAGE_DONOTCLIP。</span><span class="sxs-lookup"><span data-stu-id="6e865-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="6e865-133">在此情況下，可能需要在繪圖時執行額外的軟體裁剪，以要求在系統記憶體中有頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6e865-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="6e865-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="6e865-135">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="6e865-135">0x00000400L</span></span></td>
<td><span data-ttu-id="6e865-136">裝置支援暫時註冊的 <a href="d3dta.md">D3DTA</a> 。</span><span class="sxs-lookup"><span data-stu-id="6e865-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="6e865-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="6e865-138">0x00000800L</span><span class="sxs-lookup"><span data-stu-id="6e865-138">0x00000800L</span></span></td>
<td><span data-ttu-id="6e865-139">裝置除了 D3DBLENDOP_ADD 之外，也支援 Alpha 混色作業。</span><span class="sxs-lookup"><span data-stu-id="6e865-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-140">D3DPMISCCAPS_NullREFERENCE</span><span class="sxs-lookup"><span data-stu-id="6e865-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="6e865-141">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="6e865-141">0x00000100L</span></span></td>
<td><span data-ttu-id="6e865-142">未轉譯的參考裝置。</span><span class="sxs-lookup"><span data-stu-id="6e865-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="6e865-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="6e865-144">0x00004000L</span><span class="sxs-lookup"><span data-stu-id="6e865-144">0x00004000L</span></span></td>
<td><span data-ttu-id="6e865-145">裝置支援多個元素紋理或多個呈現目標的獨立寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="6e865-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="6e865-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="6e865-147">0x00008000L</span><span class="sxs-lookup"><span data-stu-id="6e865-147">0x00008000L</span></span></td>
<td><span data-ttu-id="6e865-148">裝置支援每一階段的常數。</span><span class="sxs-lookup"><span data-stu-id="6e865-148">Device supports per-stage constants.</span></span> <span data-ttu-id="6e865-149">請參閱 <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>中的 D3DTSS_CONSTANT。</span><span class="sxs-lookup"><span data-stu-id="6e865-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="6e865-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="6e865-151">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="6e865-151">0x00200000L</span></span></td>
<td><span data-ttu-id="6e865-152">裝置支援在混合之後轉換成 sRGB。</span><span class="sxs-lookup"><span data-stu-id="6e865-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6e865-153">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="6e865-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="6e865-154">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="6e865-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="6e865-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="6e865-156">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="6e865-156">0x00010000L</span></span></td>
<td><span data-ttu-id="6e865-157">裝置支援個別的霧化和反射 Alpha。</span><span class="sxs-lookup"><span data-stu-id="6e865-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="6e865-158">許多裝置都會使用反射 Alpha 通道來儲存霧化因數。</span><span class="sxs-lookup"><span data-stu-id="6e865-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="6e865-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="6e865-160">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="6e865-160">0x00020000L</span></span></td>
<td><span data-ttu-id="6e865-161">裝置支援 Alpha 通道的不同 blend 設定。</span><span class="sxs-lookup"><span data-stu-id="6e865-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="6e865-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="6e865-163">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="6e865-163">0x00040000L</span></span></td>
<td><span data-ttu-id="6e865-164">裝置針對多個呈現目標支援不同的位深度。</span><span class="sxs-lookup"><span data-stu-id="6e865-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e865-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="6e865-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="6e865-166">0x00080000L</span><span class="sxs-lookup"><span data-stu-id="6e865-166">0x00080000L</span></span></td>
<td><span data-ttu-id="6e865-167">裝置支援多個呈現目標的後置圖元著色器作業。</span><span class="sxs-lookup"><span data-stu-id="6e865-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e865-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="6e865-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="6e865-169">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="6e865-169">0x00100000L</span></span></td>
<td><span data-ttu-id="6e865-170">裝置個會對每個頂點的 blend 因數進行霧化。</span><span class="sxs-lookup"><span data-stu-id="6e865-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6e865-171">[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 PrimitiveMiscCaps 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="6e865-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="6e865-172">常數資訊</span><span class="sxs-lookup"><span data-stu-id="6e865-172">Constant Information</span></span>



| <span data-ttu-id="6e865-173">需求</span><span class="sxs-lookup"><span data-stu-id="6e865-173">Requirement</span></span>                         |  <span data-ttu-id="6e865-174">值</span><span class="sxs-lookup"><span data-stu-id="6e865-174">Value</span></span>          |
|--------------------------|------------|
| <span data-ttu-id="6e865-175">標頭</span><span class="sxs-lookup"><span data-stu-id="6e865-175">Header</span></span>                   | <span data-ttu-id="6e865-176">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="6e865-176">d3d9caps.h</span></span> |
| <span data-ttu-id="6e865-177">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="6e865-177">Minimum operating system</span></span> | <span data-ttu-id="6e865-178">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6e865-178">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6e865-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e865-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e865-180">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="6e865-180">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
