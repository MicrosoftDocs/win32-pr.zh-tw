---
description: D3DPRESENT 參數所使用的常數 \_ 。
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970324"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="7d591-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="7d591-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="7d591-104">[**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="7d591-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-105">#定義</span><span class="sxs-lookup"><span data-stu-id="7d591-105">#define</span></span></td>
<td><span data-ttu-id="7d591-106">值</span><span class="sxs-lookup"><span data-stu-id="7d591-106">Value</span></span></td>
<td><span data-ttu-id="7d591-107">描述</span><span class="sxs-lookup"><span data-stu-id="7d591-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d591-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="7d591-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="7d591-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7d591-109">0x00000004</span></span></td>
<td><span data-ttu-id="7d591-110">在建立 Direct3D 裝置的視訊卡的 [監視器] 畫面區域內，將視窗內的 <a href="/windows/desktop/api"><strong>現有</strong></a> array.blit 裁剪到視窗工作區中。</span><span class="sxs-lookup"><span data-stu-id="7d591-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="7d591-111">D3DPRESENTFLAG_DEVICECLIP 對 D3DSWAPEFFECT_FLIPEX 無效。</span><span class="sxs-lookup"><span data-stu-id="7d591-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d591-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="7d591-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="7d591-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7d591-113">0x00000002</span></span></td>
<td><span data-ttu-id="7d591-114">建立裝置或交換鏈時，請設定此旗標，以啟用 z 緩衝區捨棄。</span><span class="sxs-lookup"><span data-stu-id="7d591-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="7d591-115">如果設定此旗標，深度樣板緩衝區的內容在呼叫 <a href="/windows/desktop/api"><strong>其中一個或</strong></a>具有不同深度介面的 <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> 之後將會無效。</span><span class="sxs-lookup"><span data-stu-id="7d591-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="7d591-116">捨棄 z 緩衝區資料可能會提高效能，並且與驅動程式相依。</span><span class="sxs-lookup"><span data-stu-id="7d591-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="7d591-117">偵錯工具執行時間將會在 <a href="/windows/desktop/api"><strong>呼叫任一值</strong></a>之後，將 z 緩衝區清除為某個常數值，或使用不同的深度介面 <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> 來強制捨棄。</span><span class="sxs-lookup"><span data-stu-id="7d591-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="7d591-118">捨棄 z 緩衝區資料對於所有可鎖定格式（D3DFMT_D16_LOCKABLE 和 D3DFMT_D32F_LOCKABLE 而言不合法。</span><span class="sxs-lookup"><span data-stu-id="7d591-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="7d591-119">任何使用指定可鎖定格式和 z 緩衝區捨棄的 <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="7d591-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="7d591-120">如需有關格式的詳細資訊，請參閱 <a href="d3dformat.md">D3DFORMAT</a>。</span><span class="sxs-lookup"><span data-stu-id="7d591-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d591-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="7d591-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="7d591-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d591-122">0x00000001</span></span></td>
<td><span data-ttu-id="7d591-123">如果應用程式需要能夠直接鎖定背景緩衝區，請設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="7d591-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="7d591-124">請注意，除非應用程式在呼叫 <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> 或 <a href="/windows/desktop/api"><strong>重設</strong></a>時指定 D3DPRESENTFLAG_LOCKABLE_BACKBUFFER，否則無法鎖定背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7d591-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="7d591-125">在某些圖形硬體設定上，「鎖定回緩衝區」會產生效能成本。</span><span class="sxs-lookup"><span data-stu-id="7d591-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="7d591-126"> (或使用 <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> 在可鎖定的緩衝區上執行鎖定作業來寫入) ，會降低許多卡片的效能。</span><span class="sxs-lookup"><span data-stu-id="7d591-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="7d591-127">在此情況下，請考慮使用紋理三角形將資料移至背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7d591-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-128">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7d591-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d591-129">在 Direct3D9Ex 中，如果 D3DSWAPEFFECT 是 D3DSWAPEFFECT_FLIPEX，就無法設定這個旗標，因為 flip 模型可讓桌面視窗管理員存取應用程式的背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7d591-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="7d591-130">跨進程的共用介面不應鎖定。</span><span class="sxs-lookup"><span data-stu-id="7d591-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d591-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="7d591-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="7d591-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="7d591-132">0x00000020</span></span></td>
<td><span data-ttu-id="7d591-133">旋轉的監視器會在簡報期間以旋轉複製自動處理，這並不是非常有效率。</span><span class="sxs-lookup"><span data-stu-id="7d591-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="7d591-134">此旗標表示應用程式會執行它自己的顯示旋轉。</span><span class="sxs-lookup"><span data-stu-id="7d591-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-135">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7d591-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d591-136">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="7d591-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="7d591-137">應用程式可以使用旋轉的視圖矩陣來達成自己的旋轉。</span><span class="sxs-lookup"><span data-stu-id="7d591-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="7d591-138">應使用 <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> 和 <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> 方法來尋找目前的旋轉設定。</span><span class="sxs-lookup"><span data-stu-id="7d591-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="7d591-139"><a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a>和<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a>中的背景緩衝區寬度和高度參數必須使用橫向方向，而全螢幕顯示模式結構應該與 (<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a>傳回的相同，也就是在旋轉90和270度) 時，會交換寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="7d591-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="7d591-140">當您在旋轉轉譯目標上使用鎖定時，左上角的假設不會再保留 true，因此，轉譯目標 SURFACE_DESC 將維持在建立參數) （以及 GDI 視窗、滑鼠座標）所隱含的橫向 (，而且在搭配 Direct3D 轉譯目標和場景使用時必須適當地轉譯。</span><span class="sxs-lookup"><span data-stu-id="7d591-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d591-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="7d591-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="7d591-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="7d591-142">0x00000040</span></span></td>
<td><span data-ttu-id="7d591-143">您可以使用此旗標來指定顯示介面卡所列舉的任何原始顯示模式，即使 Direct3D 可能指出模式無效也一樣。</span><span class="sxs-lookup"><span data-stu-id="7d591-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="7d591-144">應用程式應該以健全的方式來執行這項工作，以防需要的模式確實無效。</span><span class="sxs-lookup"><span data-stu-id="7d591-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-145">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7d591-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d591-146">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="7d591-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d591-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="7d591-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="7d591-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7d591-148">0x00000010</span></span></td>
<td><span data-ttu-id="7d591-149">這是驅動程式的提示，其中的後端緩衝區將包含影片資料。</span><span class="sxs-lookup"><span data-stu-id="7d591-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d591-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="7d591-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="7d591-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="7d591-151">0x00000080</span></span></td>
<td><span data-ttu-id="7d591-152">指定覆迭是完整範圍的 RGB 或有限的範圍 RGB。</span><span class="sxs-lookup"><span data-stu-id="7d591-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="7d591-153">設定此旗標會指出有限的範圍 RGB。</span><span class="sxs-lookup"><span data-stu-id="7d591-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="7d591-154">在有限範圍的 RGB 中，RGB 範圍會壓縮，因此16:16:16 為黑色，而235:235:235 是白色。</span><span class="sxs-lookup"><span data-stu-id="7d591-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-155">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7d591-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d591-156">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="7d591-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d591-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="7d591-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="7d591-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="7d591-158">0x00000100</span></span></td>
<td><span data-ttu-id="7d591-159">指定重迭是否為 BT. 601 或 BT. 709。</span><span class="sxs-lookup"><span data-stu-id="7d591-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="7d591-160">設定此旗標表示709，適用于高定義電視 (HDTV) 。</span><span class="sxs-lookup"><span data-stu-id="7d591-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-161">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7d591-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d591-162">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="7d591-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d591-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="7d591-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="7d591-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="7d591-164">0x00000200</span></span></td>
<td><span data-ttu-id="7d591-165">指定覆迭是否為傳統 YCbCr 或擴充的 YCbCr (xvYCC) 。</span><span class="sxs-lookup"><span data-stu-id="7d591-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="7d591-166">設定此旗標表示擴充的 YCbCr (xvYCC) 。</span><span class="sxs-lookup"><span data-stu-id="7d591-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-167">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7d591-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d591-168">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="7d591-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d591-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="7d591-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="7d591-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="7d591-170">0x00000400</span></span></td>
<td><span data-ttu-id="7d591-171">設定此旗標表示 swapchain 包含受保護的內容，並自動使執行時間限制對 swapchain 的存取，如此一來，只有桌面 Windows 管理員 (DWM) 可以使用 swapchain。</span><span class="sxs-lookup"><span data-stu-id="7d591-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-172">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7d591-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d591-173">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="7d591-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d591-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="7d591-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="7d591-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="7d591-175">0x00000800</span></span></td>
<td><span data-ttu-id="7d591-176">設定此旗標表示驅動程式應該限制對針對 DWM 互動所建立之任何共用資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="7d591-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="7d591-177">呼叫端必須使用驅動程式來建立已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="7d591-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="7d591-178">然後，驅動程式應該允許存取嘗試開啟這些共用資源的進程。</span><span class="sxs-lookup"><span data-stu-id="7d591-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d591-179">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="7d591-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="7d591-180">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="7d591-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7d591-181">這些常數會由 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)使用。</span><span class="sxs-lookup"><span data-stu-id="7d591-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="7d591-182">常數資訊</span><span class="sxs-lookup"><span data-stu-id="7d591-182">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="7d591-183">標頭</span><span class="sxs-lookup"><span data-stu-id="7d591-183">Header</span></span>                   | <span data-ttu-id="7d591-184">d3d9types。h</span><span class="sxs-lookup"><span data-stu-id="7d591-184">d3d9types.h</span></span> |
| <span data-ttu-id="7d591-185">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="7d591-185">Minimum operating system</span></span> | <span data-ttu-id="7d591-186">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7d591-186">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="7d591-187">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d591-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d591-188">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="7d591-188">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




