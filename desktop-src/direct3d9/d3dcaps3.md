---
description: 驅動程式功能旗標。
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991647"
---
# <a name="d3dcaps3"></a><span data-ttu-id="f97ae-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="f97ae-103">D3DCAPS3</span></span>

<span data-ttu-id="f97ae-104">驅動程式功能旗標。</span><span class="sxs-lookup"><span data-stu-id="f97ae-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f97ae-105">#定義</span><span class="sxs-lookup"><span data-stu-id="f97ae-105">#define</span></span></td>
<td><span data-ttu-id="f97ae-106">值</span><span class="sxs-lookup"><span data-stu-id="f97ae-106">Value</span></span></td>
<td><span data-ttu-id="f97ae-107">描述</span><span class="sxs-lookup"><span data-stu-id="f97ae-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f97ae-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="f97ae-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="f97ae-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="f97ae-109">0x00000020L</span></span></td>
<td><span data-ttu-id="f97ae-110">指出當使用翻轉或捨棄交換效果時，裝置可以使用全螢幕模式下的 D3DRS_ALPHABLENDENABLE 呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="f97ae-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="f97ae-111">只有當 D3DRS_SRCBLEND 或 D3DRS_DESTBLEND 狀態設定為下列其中一項時，才適用這種情況：</span><span class="sxs-lookup"><span data-stu-id="f97ae-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="f97ae-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="f97ae-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="f97ae-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="f97ae-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="f97ae-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="f97ae-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="f97ae-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="f97ae-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f97ae-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="f97ae-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="f97ae-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="f97ae-117">0x00000100L</span></span></td>
<td><span data-ttu-id="f97ae-118">裝置可以加速從系統記憶體複製到本機視訊記憶體的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f97ae-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="f97ae-119">此上限可確保 <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> 和 <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> 呼叫將會是硬體加速。</span><span class="sxs-lookup"><span data-stu-id="f97ae-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="f97ae-120">如果不存在此上限，則這些呼叫會成功，但速度會變慢。</span><span class="sxs-lookup"><span data-stu-id="f97ae-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f97ae-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="f97ae-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="f97ae-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="f97ae-122">0x00000200L</span></span></td>
<td><span data-ttu-id="f97ae-123">裝置可以加速從本機視訊記憶體到系統記憶體的記憶體複製。</span><span class="sxs-lookup"><span data-stu-id="f97ae-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="f97ae-124">此上限可保證 <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> 呼叫將會是硬體加速。</span><span class="sxs-lookup"><span data-stu-id="f97ae-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="f97ae-125">如果不存在此上限，此呼叫將會成功，但會變慢。</span><span class="sxs-lookup"><span data-stu-id="f97ae-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f97ae-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="f97ae-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="f97ae-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="f97ae-127">0x00000400L</span></span></td>
<td><span data-ttu-id="f97ae-128">顯示驅動程式支援 DXVA-HD DDI。</span><span class="sxs-lookup"><span data-stu-id="f97ae-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="f97ae-129">如需 DXVA-HD DDI 的詳細資訊，請參閱 <a href="https://msdn.microsoft.com/library/dd835176.aspx">處理 High-Definition 影片</a>。</span><span class="sxs-lookup"><span data-stu-id="f97ae-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f97ae-130">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="f97ae-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="f97ae-131">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="f97ae-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f97ae-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="f97ae-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="f97ae-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="f97ae-133">0x00000080L</span></span></td>
<td><span data-ttu-id="f97ae-134">指出裝置可以從視窗型背景緩衝區執行 gamma 修正， (包含) 至 sRGB 桌面的線性內容。</span><span class="sxs-lookup"><span data-stu-id="f97ae-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f97ae-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="f97ae-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="f97ae-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="f97ae-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="f97ae-137">保護未使用。</span><span class="sxs-lookup"><span data-stu-id="f97ae-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f97ae-138">[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 D3CAPS3 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="f97ae-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="f97ae-139">常數資訊</span><span class="sxs-lookup"><span data-stu-id="f97ae-139">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f97ae-140">標頭</span><span class="sxs-lookup"><span data-stu-id="f97ae-140">Header</span></span>                   | <span data-ttu-id="f97ae-141">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="f97ae-141">d3d9caps.h</span></span> |
| <span data-ttu-id="f97ae-142">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="f97ae-142">Minimum operating system</span></span> | <span data-ttu-id="f97ae-143">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f97ae-143">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f97ae-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="f97ae-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f97ae-145">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="f97ae-145">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




