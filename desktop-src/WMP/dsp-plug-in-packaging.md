---
title: DSP 外掛程式封裝
description: DSP 外掛程式封裝
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Windows Media Player 外掛程式，媒體基礎管線
- 外掛程式，媒體基礎管線
- 數位信號處理外掛程式，媒體基礎管線
- DSP 外掛程式，媒體基礎管線
- 媒體基礎管線
- Windows Media Player 外掛程式、DirectShow 管線
- 外掛程式，DirectShow 管線
- 數位信號處理外掛程式，DirectShow 管線
- DSP 外掛程式，DirectShow 管線
- DirectShow 管線
- 數位信號處理外掛程式，基本
- DSP 外掛程式，基本
- Windows Media Player 外掛程式，基本 DSP
- 外掛程式，基本 DSP
- 基本的 DSP 外掛程式
- Windows Media Player 外掛程式、雙重模式的 DSP
- 外掛程式、雙重模式的 DSP
- 數位信號處理外掛程式、雙重模式
- DSP 外掛程式、雙重模式
- 雙重模式的 DSP 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106995566"
---
# <a name="dsp-plug-in-packaging"></a><span data-ttu-id="ea8fb-123">DSP 外掛程式封裝</span><span class="sxs-lookup"><span data-stu-id="ea8fb-123">DSP Plug-in Packaging</span></span>

<span data-ttu-id="ea8fb-124">Windows Media Player 使用下列其中一個管線呈現音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-124">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="ea8fb-125">DirectShow</span><span class="sxs-lookup"><span data-stu-id="ea8fb-125">DirectShow</span></span>
-   <span data-ttu-id="ea8fb-126">媒體基礎</span><span class="sxs-lookup"><span data-stu-id="ea8fb-126">Media Foundation</span></span>

<span data-ttu-id="ea8fb-127">在 Microsoft Windows XP 及更早版本中，Player 會使用 DirectShow。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-127">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="ea8fb-128">在 Windows Vista 中，播放的有時會使用 DirectShow，有時會使用媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-128">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="ea8fb-129">專為在 DirectShow 管線中執行而設計的 DSP 外掛程式，稱為 *基本的 dsp 外掛程式*。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-129">A DSP plug-in that is designed to run in the DirectShow pipeline is called a *basic DSP plug-in*.</span></span> <span data-ttu-id="ea8fb-130">基本的 DSP 外掛程式可作為 DirectX 媒體物件 (的) 。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-130">A basic DSP plug-ins acts as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="ea8fb-131">基本的 DSP 外掛程式可在 DirectShow 管線中以原生方式執行，也可以在媒體基礎所提供包裝函式內的媒體基礎管線中執行。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-131">A basic DSP plug-in can run natively in the DirectShow pipeline and can also run in the Media Foundation pipeline inside a wrapper provided by Media Foundation.</span></span>

<span data-ttu-id="ea8fb-132">DSP 外掛程式的設計目的是要以原生方式執行 (在 DirectShow 和媒體基礎管線中都不需要包裝函式) ，稱為 *雙重模式的 DSP 外掛程式*。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-132">A DSP plug-in that is designed to run natively (no wrapper required) in both the DirectShow and Media Foundation pipelines is called a *dual-mode DSP plug-in*.</span></span> <span data-ttu-id="ea8fb-133">雙重模式的 DSP 外掛程式可作為一或媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-133">A dual-mode DSP plug-in can act as a DMO or as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="ea8fb-134">DSP 外掛程式是封裝為自我註冊 .dll 檔案的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-134">A DSP plug-in is a COM object that is packaged as a self-registering .dll file.</span></span> <span data-ttu-id="ea8fb-135">外掛程式所執行的介面，取決於外掛程式是否設計為基本的 DSP 外掛程式或雙重模式的 DSP 外掛程式而定。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-135">The interfaces that the plug-in implements depend on whether the plug-in is designed as a basic DSP plug-in or as a dual-mode DSP plug-in.</span></span> <span data-ttu-id="ea8fb-136">如需有關 DSP 外掛程式必須執行之介面的詳細資訊，請參閱 [必要的介面](required-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-136">For detailed information about the interfaces that DSP plug-ins must implement, see [Required Interfaces](required-interfaces.md).</span></span>

<span data-ttu-id="ea8fb-137">在媒體基礎管線中執行的 DSP 外掛程式 (原生或包裝) 必須將其執行緒模型註冊為 "Both"。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-137">A DSP plug-in that runs in the Media Foundation pipeline (either natively or wrapped) must register its threading model as "Both".</span></span> <span data-ttu-id="ea8fb-138">如需有關登錄子機碼和與 DSP 外掛程式相關聯之專案的詳細資訊，請參閱 [註冊 Dsp 外掛程式](registering-dsp-plug-ins.md)。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-138">For detailed information about registry subkeys and entries associated with DSP plug-ins, see [Registering DSP Plug-ins](registering-dsp-plug-ins.md).</span></span>

<span data-ttu-id="ea8fb-139">在媒體基礎管線中執行自訂介面和執行的 DSP 外掛程式 (原生或包裝) 必須與可封送處理跨進程界限的自訂介面的 proxy stub .dll 檔配對。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-139">A DSP plug-in that implements custom interfaces and runs in the Media Foundation pipeline (either natively or wrapped) must be paired with a proxy-stub .dll file that can marshal the custom interfaces across process boundaries.</span></span> <span data-ttu-id="ea8fb-140">如需 proxy 存根元件的詳細資訊，請參閱 Windows Media Player 11 的將 [現有的 Dsp 外掛程式](updating-existing-dsp-plug-ins.md) 和 [更新加入至 Dsp 外掛程式的更新](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-140">For information about the proxy-stub component, see [Updating Existing DSP Plug-ins](updating-existing-dsp-plug-ins.md) and [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span>

<span data-ttu-id="ea8fb-141">DSP 外掛程式物件不得建立為 singleton。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-141">DSP plug-in objects must not be created as singletons.</span></span> <span data-ttu-id="ea8fb-142">Windows Media Player 必須能夠建立特定 DSP 外掛程式的多個個別實例。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-142">Windows Media Player must be able to create multiple separate instances of a particular DSP plug-in.</span></span>

<span data-ttu-id="ea8fb-143">在 Windows Vista 受保護媒體路徑中執行的 DSP 外掛程式 (PMP) 必須經過簽署。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-143">DSP plug-ins that run in the Windows Vista Protected Media Path (PMP) must be signed.</span></span> <span data-ttu-id="ea8fb-144">如需詳細資訊，請參閱 [Windows Vista 中受保護媒體元件的程式碼簽署](/windows-hardware/test/hlk/)。</span><span class="sxs-lookup"><span data-stu-id="ea8fb-144">For more information, see [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea8fb-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea8fb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea8fb-146">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="ea8fb-146">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 