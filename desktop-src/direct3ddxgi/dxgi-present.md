---
description: DXGI \_ 存在常數指定了在輸出中呈現畫面格的選項。
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: 'DXGI_PRESENT (DXGI. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a21d53159572a52b372774e4988e775744ede5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992707"
---
# <a name="dxgi_present"></a><span data-ttu-id="4ea8b-103">DXGI \_ 存在</span><span class="sxs-lookup"><span data-stu-id="4ea8b-103">DXGI\_PRESENT</span></span>

<span data-ttu-id="4ea8b-104">**DXGI \_ 存在** 常數指定了在輸出中呈現畫面格的選項。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-104">The **DXGI\_PRESENT** constants specify options for presenting frames to the output.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4ea8b-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="4ea8b-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4ea8b-106">Description</span><span class="sxs-lookup"><span data-stu-id="4ea8b-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span></span><dl> <span data-ttu-id="4ea8b-107"><dt><strong></strong></dt><dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-107"><dt><strong></strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-108">顯示每個緩衝區的框架 (從目前的緩衝區) 到輸出。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-108">Present a frame from each buffer (starting with the current buffer) to the output.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <span data-ttu-id="4ea8b-109"><dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-109"><dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-110">將目前緩衝區中的畫面格呈現給輸出。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-110">Present a frame from the current buffer to the output.</span></span> <span data-ttu-id="4ea8b-111">使用這個旗標，讓簡報可以使用垂直空白的同步處理，而不是以一般方式來排序鏈中的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-111">Use this flag so that the presentation can use vertical-blank synchronization instead of sequencing buffers in the chain in the usual manner.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ea8b-112">如果呼叫的應用程式在第一個目前的作業上設定 DXGI_PRESENT_DO_NOT_SEQUENCE 常數 (亦即，當沒有目前的緩衝區) 時，執行時間會忽略目前的作業，而不會呼叫驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-112">If the calling application sets the DXGI_PRESENT_DO_NOT_SEQUENCE constant on the first present operation (that is, when there is no current buffer), the runtime ignores that present operation and does not call the driver.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <span data-ttu-id="4ea8b-113"><dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-113"><dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-114">不要將框架呈現在輸出中。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-114">Do not present the frame to the output.</span></span> <span data-ttu-id="4ea8b-115">交換鏈的狀態將會經過測試，並傳回適當的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-115">The status of the swap chain will be tested and appropriate errors returned.</span></span> <span data-ttu-id="4ea8b-116">DXGI_PRESENT_TEST 僅適用于從閒置狀態切換時：請勿使用它來判斷何時切換為閒置狀態，因為這樣做可能會讓交換鏈無法結束全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-116">DXGI_PRESENT_TEST is intended for use only when switching from the idle state; do not use it to determine when to switch to the idle state because doing so can leave the swap chain unable to exit full-screen mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <span data-ttu-id="4ea8b-117"><dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-117"><dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-118">指定執行時間將捨棄未完成的佇列呈現。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-118">Specifies that the runtime will discard outstanding queued presents.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <span data-ttu-id="4ea8b-119"><dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-119"><dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-120">指定執行時間將會使簡報失敗 (也就是當呼叫的執行緒遭到封鎖時，將呼叫 <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1：:P resent1</strong></a>) ，並 <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> 錯誤碼。執行時間會傳回 DXGI_ERROR_WAS_STILL_DRAWING 而非睡眠，直到解決相依性為止。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-120">Specifies that the runtime will fail the presentation (that is, fail a call to <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::Present1</strong></a>) with the <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> error code if the calling thread is blocked; the runtime returns DXGI_ERROR_WAS_STILL_DRAWING instead of sleeping until the dependency is resolved.</span></span><br/> <span data-ttu-id="4ea8b-121"><strong>Direct3D 11：</strong> 從 Windows 8 開始支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-121"><strong>Direct3D 11:</strong> This enumeration value is supported starting with Windows 8.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <span data-ttu-id="4ea8b-122"><dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-122"><dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-123">表示只會在特定輸出上顯示簡報內容。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-123">Indicates that presentation content will be shown only on the particular output.</span></span> <span data-ttu-id="4ea8b-124">內容將不會顯示在其他輸出上。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-124">The content will not be visible on other outputs.</span></span> <span data-ttu-id="4ea8b-125">例如，如果使用者嘗試在其他輸出上重新放置影片內容，則不會顯示影片內容。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-125">For example, if the user tries to relocate video content on another output, the video content will not be visible.</span></span> <br/> <span data-ttu-id="4ea8b-126"><strong>Direct3D 11：</strong> 從 Windows 8 開始支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-126"><strong>Direct3D 11:</strong> This enumeration value is supported starting with Windows 8.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ea8b-127">此旗標只能搭配 <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> 或 DXGI_SWAP_EFFECT_FLIP_DISCARD 的交換效果使用。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-127">This flag should only be used with swap effect <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> or DXGI_SWAP_EFFECT_FLIP_DISCARD.</span></span> <span data-ttu-id="4ea8b-128">此旗標與 <em>其他</em> 交換效果的用法已被取代，在未來的 Windows 版本中可能無法運作。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-128">The use of this flag with <em>other</em> swap effects is being deprecated, and may not work in future versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <span data-ttu-id="4ea8b-129"><dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-129"><dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-130">指出如果身歷聲存在必須縮小為 mono，則會使用靠右的觀賞，而不是左方的觀賞。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-130">Indicates that if the stereo present must be reduced to mono, right-eye viewing is used rather than left-eye viewing.</span></span><br/> <span data-ttu-id="4ea8b-131"><strong>Direct3D 11：</strong> 從 Windows 8 開始支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-131"><strong>Direct3D 11:</strong> This enumeration value is supported starting with Windows 8.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <span data-ttu-id="4ea8b-132"><dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-132"><dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-133">指出簡報應使用左邊的緩衝區做為 mono 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-133">Indicates that the presentation should use the left buffer as a mono buffer.</span></span> <span data-ttu-id="4ea8b-134">應用程式會呼叫 <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1：： IsTemporaryMonoSupported</strong></a> 方法，以判斷交換鏈是否支援 &quot; 暫存 mono &quot; 。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-134">An application calls the <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1::IsTemporaryMonoSupported</strong></a> method to determine whether a swap chain supports &quot;temporary mono&quot;.</span></span><br/> <span data-ttu-id="4ea8b-135"><strong>Direct3D 11：</strong> 從 Windows 8 開始支援這個列舉值。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-135"><strong>Direct3D 11:</strong> This enumeration value is supported starting with Windows 8.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <span data-ttu-id="4ea8b-136"><dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-136"><dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-137">此旗標必須由目前使用自訂持續時間 (自訂重新整理頻率) 的媒體應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-137">This flag must be set by media apps that are currently using a custom present duration (custom refresh rate).</span></span> <span data-ttu-id="4ea8b-138">請參閱 <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-138">See <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ea8b-139">從 Windows 8.1 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-139">This value is supported starting in Windows 8.1.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <span data-ttu-id="4ea8b-140"><dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </span><span class="sxs-lookup"><span data-stu-id="4ea8b-140"><dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4ea8b-141">允許卸載是變數重新整理頻率顯示的需求。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-141">Allowing tearing is a requirement of variable refresh rate displays.</span></span><br/> <span data-ttu-id="4ea8b-142">在目前使用 DXGI_PRESENT_ALLOW_TEARING 的條件如下所示：</span><span class="sxs-lookup"><span data-stu-id="4ea8b-142">The conditions for using DXGI_PRESENT_ALLOW_TEARING during Present are as follows:</span></span><br/>
<ul>
<li><span data-ttu-id="4ea8b-143">交換鏈必須使用 <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> 旗標來建立。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-143">The swap chain must be created with the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> flag.</span></span></li>
<li><span data-ttu-id="4ea8b-144">傳入 <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>的同步間隔 (或</strong></a> <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) 必須是0。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-144">The sync interval passed in to <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Present</strong></a> (or <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) must be 0.</span></span></li>
<li><span data-ttu-id="4ea8b-145">DXGI_PRESENT_ALLOW_TEARING 旗標不能用在目前處於全螢幕獨佔模式的應用程式中 (由呼叫 <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState (TRUE) </strong></a>) 來設定。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-145">The DXGI_PRESENT_ALLOW_TEARING flag cannot be used in an application that is currently in full screen exclusive mode (set by calling <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState(TRUE)</strong></a>).</span></span> <span data-ttu-id="4ea8b-146">只能在視窗模式中使用。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-146">It can only be used in windowed mode.</span></span> <span data-ttu-id="4ea8b-147">若要在全螢幕 Win32 應用程式中使用此旗標，應用程式應該會出現在全螢幕無邊框的視窗中，並使用 <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory：： MakeWindowAssociation</strong></a>停用自動 ALT + ENTER 全螢幕切換。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-147">To use this flag in full screen Win32 apps, the application should present to a fullscreen borderless window and disable automatic ALT+ENTER fullscreen switching using <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory::MakeWindowAssociation</strong></a>.</span></span> <span data-ttu-id="4ea8b-148">藉由呼叫進入全螢幕模式的 UWP 應用程式 <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> 是全螢幕無邊框的視窗，而且可能會使用旗標。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-148">UWP apps that enter fullscreen mode by calling <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> are fullscreen borderless windows and may use the flag.</span></span></li>
</ul>
<span data-ttu-id="4ea8b-149">使用這個旗標 <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>來呼叫 (</strong></a> 或 <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) ，而不符合上述條件，將會導致 DXGI_ERROR_INVALID_CALL 錯誤傳回給呼叫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-149">Calling <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Present</strong></a> (or <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) with this flag and not meeting the conditions above will result in a DXGI_ERROR_INVALID_CALL error being returned to the calling application.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="4ea8b-150">備註</span><span class="sxs-lookup"><span data-stu-id="4ea8b-150">Remarks</span></span>

<span data-ttu-id="4ea8b-151">在 IDXGISwapChain 期間會提供展示選項 [**：:P**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) 重新傳送或 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-151">Presentation options are supplied during the [**IDXGISwapChain::Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) or [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) call.</span></span> <span data-ttu-id="4ea8b-152">緩衝區會在交換鏈描述中指定 (請參閱 [**DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) 或 [**dxgi \_ 交換 \_ 鏈 \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)) 。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-152">The buffers are specified in the swap chain description (see [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) or [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)).</span></span>

<span data-ttu-id="4ea8b-153">DXGI \_ 存在 \_ 重新開機僅適用于翻轉模型交換鏈和全螢幕。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-153">DXGI\_PRESENT\_RESTART is valid only for flip-model swap chains and full screen.</span></span> <span data-ttu-id="4ea8b-154">應用程式可以使用 DXGI \_ 存在 \_ 重新開機來復原播放中的問題，以及捨棄之前排入佇列的簡報。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-154">Applications can use DXGI\_PRESENT\_RESTART to recover from glitches in playback, as well as to discard previously queued presentations.</span></span> <span data-ttu-id="4ea8b-155">如果已排入佇列的簡報是視窗化的案例，捨棄之前排入佇列的簡報會很</span><span class="sxs-lookup"><span data-stu-id="4ea8b-155">Discarding previously queued presentations is useful if those queued presentations are windowed scenarios.</span></span> <span data-ttu-id="4ea8b-156">特別是，先前排入佇列的簡報可能會假設視窗是舊的大小 (也就是在提交) 之後發生調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-156">In particular, the previously queued presentation might have assumed that the window is an old size (that is, a resize operation occurred after submission).</span></span>

<span data-ttu-id="4ea8b-157">DXGI \_ 存在 \_ 限制 \_ \_ 輸出僅適用于指定特定輸出的交換鏈，可在建立這些交換鏈時限制內容， ([**IDXGIFactory2：： CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)) 。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-157">DXGI\_PRESENT\_RESTRICT\_TO\_OUTPUT is valid only for swap chains that specified a particular output to restrict content to when those swap chains were created ([**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)).</span></span> <span data-ttu-id="4ea8b-158">如果沒有要限制的輸出，旗標就會無效。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-158">If there is no output to restrict to, the flag is invalid.</span></span>

<span data-ttu-id="4ea8b-159">DXGI \_ 出現 \_ \_ 的立體慣用 \_ ，表示如果身歷聲存在必須縮減為 mono，則應該使用適當的眼睛，而不是左方 (預設) 眼。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-159">DXGI\_PRESENT\_STEREO\_PREFER\_RIGHT indicates that if the stereo present must be reduced to mono the right eye should be used rather than the left (default) eye.</span></span> <span data-ttu-id="4ea8b-160">如果有一側的品質較高，您可以使用此旗標 (例如，如果身歷聲組是從標準映射合成的，則為 < ) </span><span class="sxs-lookup"><span data-stu-id="4ea8b-160">You can use this flag if one side is higher quality (for example, if the stereo pair is synthesized from a standard image.)</span></span>

<span data-ttu-id="4ea8b-161">DXGI \_ 目前 \_ \_ 的立體暫存 \_ MONO 指出目前的緩衝區應使用左邊的緩衝區作為 MONO 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-161">DXGI\_PRESENT\_STEREO\_TEMPORARY\_MONO indicates that the present should use the left buffer as a mono buffer.</span></span> <span data-ttu-id="4ea8b-162">您可以使用此旗標，以避免在應用程式暫時沒有任何身歷聲內容時更新正確的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-162">You can use this flag to avoid updating the right buffer when an application temporarily has no stereo content.</span></span> <span data-ttu-id="4ea8b-163">您應該盡可能使用此旗標，因為它能讓作業系統大幅優化，而且在某些情況下，它可以避免可見的模式變更成品。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-163">You should use this flag whenever possible because it enables significant optimization by the operating system and under some circumstances it can avoid visible mode change artifacts.</span></span>

<span data-ttu-id="4ea8b-164">您應該 \_ 在喜好設定中使用 DXGI 目前的 \_ 身歷聲 \_ 暫存 \_ MONO 旗標，以切換至您預期會再次使用身歷聲的大部分應用程式的 MONO 交換鏈。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-164">You should use the DXGI\_PRESENT\_STEREO\_TEMPORARY\_MONO flag in preference to switching to a mono swap chain for most applications that you anticipate will use stereo again.</span></span> <span data-ttu-id="4ea8b-165">您必須在應用程式中使用此旗標，而這些應用程式的執行時間非常長，或是很少會針對未使用記憶體的缺點顯示身歷聲。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-165">You need to balance the use of this flag in applications that are extremely long running or that rarely display stereo against the disadvantage of unused memory.</span></span>

> [!Note]  
> <span data-ttu-id="4ea8b-166">切換至 mono 交換鏈的全螢幕應用程式會造成通常有可見成品 (的模式變更，例如「閃爍」 ) 。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-166">Full-screen applications that switch to a mono swap chain cause a mode change that generally has visible artifacts (for example, "flashing”).</span></span> <span data-ttu-id="4ea8b-167">不過，全螢幕交換鏈可能不支援暫存 mono。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-167">However, temporary mono might not be supported for full-screen swap chains.</span></span>

 

<span data-ttu-id="4ea8b-168">DXGI \_ 出現 \_ 身歷聲 \_ 慣用 \_ ，而 dxgi \_ 目前有 \_ 身歷聲 \_ 暫存 \_ MONO 旗標只適用于身歷聲交換鏈。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-168">The DXGI\_PRESENT\_STEREO\_PREFER\_RIGHT and DXGI\_PRESENT\_STEREO\_TEMPORARY\_MONO flags apply only to stereo swap chains.</span></span> <span data-ttu-id="4ea8b-169">如果您在顯示 mono 交換鏈時使用它們，就會發生不正確作業。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-169">If you use them when you present mono swap chains, an invalid operation occurs.</span></span>

<span data-ttu-id="4ea8b-170">如果您在 \_ \_ \_ \_ 呈現不支援臨時 MONO 的身歷聲交換鏈時使用 DXGI 出現身歷聲暫存 MONO 旗標，則會發生錯誤，交換鏈不會顯示，且簡報會傳回 [DXGI \_ 錯誤不正確 \_ \_ 呼叫](dxgi-error.md)。</span><span class="sxs-lookup"><span data-stu-id="4ea8b-170">If you use the DXGI\_PRESENT\_STEREO\_TEMPORARY\_MONO flag when you present a stereo swap chain that does not support temporary mono, an error occurs, the swap chain does not display, and the presentation returns [DXGI\_ERROR\_INVALID\_CALL](dxgi-error.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea8b-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ea8b-171">Requirements</span></span>



| <span data-ttu-id="4ea8b-172">需求</span><span class="sxs-lookup"><span data-stu-id="4ea8b-172">Requirement</span></span> | <span data-ttu-id="4ea8b-173">值</span><span class="sxs-lookup"><span data-stu-id="4ea8b-173">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4ea8b-174">標頭</span><span class="sxs-lookup"><span data-stu-id="4ea8b-174">Header</span></span><br/> | <dl> <span data-ttu-id="4ea8b-175"><dt>DXGI。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ea8b-175"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea8b-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ea8b-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea8b-177">DXGI 常數</span><span class="sxs-lookup"><span data-stu-id="4ea8b-177">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
