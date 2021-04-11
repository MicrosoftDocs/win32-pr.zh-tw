---
description: 材質篩選常數。
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c122b1260d568a43c69c336059e26a6ecfde2a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026008"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="514ee-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="514ee-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="514ee-104">材質篩選常數。</span><span class="sxs-lookup"><span data-stu-id="514ee-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="514ee-105">#定義</span><span class="sxs-lookup"><span data-stu-id="514ee-105">#define</span></span></td>
<td><span data-ttu-id="514ee-106">Description</span><span class="sxs-lookup"><span data-stu-id="514ee-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="514ee-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="514ee-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="514ee-108">裝置支援單色卷積篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="514ee-109">此篩選是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_CONVOLUTIONMONO 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="514ee-110">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="514ee-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="514ee-111">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="514ee-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="514ee-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="514ee-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="514ee-113">裝置支援對放大鏡進行每個階段的點範例篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="514ee-114">點範例的放大濾波器是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_POINT 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="514ee-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="514ee-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="514ee-116">裝置支援對放大鏡的每一階段雙線性插補篩選進行 mipmap。</span><span class="sxs-lookup"><span data-stu-id="514ee-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="514ee-117">雙線性插補 mipmap 濾波器是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_LINEAR 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="514ee-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="514ee-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="514ee-119">裝置支援對放大鏡進行的每一階段的非等向篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="514ee-120"><a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a>列舉型別的 D3DTEXF_ANISOTROPIC 成員表示非等向放大篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="514ee-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="514ee-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="514ee-122">裝置支援放大紋理的每一階段金字塔範例篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="514ee-123">金字塔放大鏡篩選會以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_PYRAMIDALQUAD 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="514ee-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="514ee-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="514ee-125">裝置支援放大紋理的每一階段高斯四次篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="514ee-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="514ee-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="514ee-127">裝置支援縮小材質的每個階段點範例篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="514ee-128">點範例縮制篩選會以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_POINT 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="514ee-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="514ee-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="514ee-130">裝置支援縮小材質的每一階段線性篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="514ee-131">線性縮制濾波器是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_LINEAR 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="514ee-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="514ee-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="514ee-133">裝置支援縮小材質的每一階段非等向篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="514ee-134">縮制篩選準則是由 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_ANISOTROPIC 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="514ee-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="514ee-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="514ee-136">裝置支援縮小材質的每一階段金字塔範例篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="514ee-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="514ee-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="514ee-138">裝置支援縮小材質的每一階段高斯四種篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="514ee-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="514ee-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="514ee-140">裝置支援 mipmap 的每個階段點範例篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="514ee-141">點範例 mipmap 篩選會以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_POINT 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="514ee-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="514ee-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="514ee-143">裝置針對 mipmap 支援每一階段的雙線性插補篩選。</span><span class="sxs-lookup"><span data-stu-id="514ee-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="514ee-144">雙線性插補 mipmap 濾波器是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_LINEAR 成員表示。</span><span class="sxs-lookup"><span data-stu-id="514ee-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="514ee-145">這些常數由 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 TextureFilterCaps、CubeTextureFilterCaps、VolumeTextureFilterCaps 和 VertexTextureFilterCaps 成員使用。</span><span class="sxs-lookup"><span data-stu-id="514ee-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="514ee-146">常數資訊</span><span class="sxs-lookup"><span data-stu-id="514ee-146">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="514ee-147">標頭</span><span class="sxs-lookup"><span data-stu-id="514ee-147">Header</span></span>                   | <span data-ttu-id="514ee-148">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="514ee-148">d3d9caps.h</span></span> |
| <span data-ttu-id="514ee-149">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="514ee-149">Minimum operating system</span></span> | <span data-ttu-id="514ee-150">Windows 98</span><span class="sxs-lookup"><span data-stu-id="514ee-150">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="514ee-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="514ee-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="514ee-152">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="514ee-152">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
