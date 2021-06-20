---
description: 查看 D3DCAPS2 驅動程式功能旗標的清單。 包含定義、值和描述，以及 Api 的連結。
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2266073c2d803f9bf11f4a3548078c0d34e5f78
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408291"
---
# <a name="d3dcaps2"></a><span data-ttu-id="749c7-104">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="749c7-104">D3DCAPS2</span></span>

<span data-ttu-id="749c7-105">驅動程式功能旗標。</span><span class="sxs-lookup"><span data-stu-id="749c7-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="749c7-106">#定義</span><span class="sxs-lookup"><span data-stu-id="749c7-106">#define</span></span></td>
<td><span data-ttu-id="749c7-107">值</span><span class="sxs-lookup"><span data-stu-id="749c7-107">Value</span></span></td>
<td><span data-ttu-id="749c7-108">描述</span><span class="sxs-lookup"><span data-stu-id="749c7-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="749c7-109">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="749c7-109">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="749c7-110">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="749c7-110">0x40000000L</span></span></td>
<td><span data-ttu-id="749c7-111">驅動程式能夠自動產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="749c7-111">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="749c7-112">如需詳細資訊，請參閱 <a href="automatic-generation-of-mipmaps.md">自動產生 mipmap (Direct3D 9) </a>。</span><span class="sxs-lookup"><span data-stu-id="749c7-112">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="749c7-113">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="749c7-113">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="749c7-114">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="749c7-114">0x00100000L</span></span></td>
<td><span data-ttu-id="749c7-115">系統已安裝校正器，可自動調整 gamma 的斜坡，使所有具有校正器的系統上的結果都相同。</span><span class="sxs-lookup"><span data-stu-id="749c7-115">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="749c7-116">若要在設定新的 gamma 層級時叫用校正器，請在呼叫 <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>時使用 D3DSGR_CALIBRATE 旗標。</span><span class="sxs-lookup"><span data-stu-id="749c7-116">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="749c7-117">校準 gamma 的斜坡會產生一些處理的額外負荷，不應經常使用。</span><span class="sxs-lookup"><span data-stu-id="749c7-117">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="749c7-118">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="749c7-118">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="749c7-119">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="749c7-119">0x80000000L</span></span></td>
<td><span data-ttu-id="749c7-120">裝置可以建立可共用的資源。</span><span class="sxs-lookup"><span data-stu-id="749c7-120">The device can create sharable resources.</span></span> <span data-ttu-id="749c7-121">建立資源的方法可以設定其 <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> 參數的非 Null 值。</span><span class="sxs-lookup"><span data-stu-id="749c7-121">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="749c7-122">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="749c7-122">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="749c7-123">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="749c7-123">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="749c7-124">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="749c7-124">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="749c7-125">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="749c7-125">0x10000000L</span></span></td>
<td><span data-ttu-id="749c7-126">驅動程式能夠管理資源。</span><span class="sxs-lookup"><span data-stu-id="749c7-126">The driver is capable of managing resources.</span></span> <span data-ttu-id="749c7-127">在這類驅動程式上，D3DPOOL_MANAGED 資源將由驅動程式管理。</span><span class="sxs-lookup"><span data-stu-id="749c7-127">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="749c7-128">若要讓 Direct3D 覆寫驅動程式，以便 Direct3D 管理資源，請在呼叫 <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>時使用 D3DCREATE_DISABLE_DRIVER_MANAGEMENT 旗標。</span><span class="sxs-lookup"><span data-stu-id="749c7-128">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="749c7-129">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="749c7-129">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="749c7-130">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="749c7-130">0x20000000L</span></span></td>
<td><span data-ttu-id="749c7-131">此驅動程式支援動態紋理。</span><span class="sxs-lookup"><span data-stu-id="749c7-131">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="749c7-132">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="749c7-132">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="749c7-133">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="749c7-133">0x00020000L</span></span></td>
<td><span data-ttu-id="749c7-134">此驅動程式支援以全螢幕模式進行動態 gamma 遞增調整。</span><span class="sxs-lookup"><span data-stu-id="749c7-134">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="749c7-135">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="749c7-135">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="749c7-136">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="749c7-136">0x02000000L</span></span></td>
<td><span data-ttu-id="749c7-137">保護未使用。</span><span class="sxs-lookup"><span data-stu-id="749c7-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="749c7-138">[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 D3CAPS2 成員會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="749c7-138">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="749c7-139">常數資訊</span><span class="sxs-lookup"><span data-stu-id="749c7-139">Constant Information</span></span>



|  <span data-ttu-id="749c7-140">需求</span><span class="sxs-lookup"><span data-stu-id="749c7-140">Requirement</span></span>                        | <span data-ttu-id="749c7-141">值</span><span class="sxs-lookup"><span data-stu-id="749c7-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="749c7-142">標頭</span><span class="sxs-lookup"><span data-stu-id="749c7-142">Header</span></span>                   | <span data-ttu-id="749c7-143">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="749c7-143">d3d9caps.h</span></span> |
| <span data-ttu-id="749c7-144">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="749c7-144">Minimum operating system</span></span> | <span data-ttu-id="749c7-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="749c7-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="749c7-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="749c7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="749c7-147">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="749c7-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
