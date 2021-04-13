---
title: 使用輸出保護層級
description: 使用輸出保護層級
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- 'Windows Media 格式 SDK、輸出保護層級 (OPL) '
- Windows Media Format SDK，保護層級
- 'Advanced Systems Format (ASF) ，輸出保護層級 (OPL) '
- 'ASF (Advanced Systems Format) ，輸出保護層級 (OPL) '
- Advanced Systems Format (ASF) 、保護等級
- ASF (Advanced Systems Format) ，保護等級
- Advanced Systems Format (ASF) 、多重授權
- ASF (Advanced Systems Format) 、多重授權
- '數位版權管理 (DRM) ，輸出保護層級 (OPL) '
- 'DRM (數位版權管理) ，輸出保護層級 (OPL) '
- 數位版權管理 (DRM) ，保護等級
- DRM (數位版權管理) ，保護等級
- '數位版權管理 (DRM) ， (OPL 評估輸出保護層級) '
- 'DRM (數位版權管理) ， (OPL 評估輸出保護層級) '
- 數位版權管理 (DRM) ，多個授權
- DRM (數位版權管理) 、多重授權
- '輸出保護層級 (OPL) '
- 'OPL (輸出保護層級) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314220"
---
# <a name="working-with-output-protection-levels"></a><span data-ttu-id="841b6-121">使用輸出保護層級</span><span class="sxs-lookup"><span data-stu-id="841b6-121">Working with Output Protection Levels</span></span>

<span data-ttu-id="841b6-122">使用 Windows Media Rights Manager 10 SDK 建立的授權可以使用輸出保護層級 (OPLs) 來指定動作限制。</span><span class="sxs-lookup"><span data-stu-id="841b6-122">Licenses created by using the Windows Media Rights Manager 10 SDK can specify action restrictions using output protection levels (OPLs).</span></span> <span data-ttu-id="841b6-123">OPLs 可讓授權建立者只允許在具有特定技術的裝置上執行某些動作。</span><span class="sxs-lookup"><span data-stu-id="841b6-123">OPLs enable a license creator to allow some actions only on devices with specific technologies.</span></span> <span data-ttu-id="841b6-124">使用 OPLs 的優點是，您在建立比舊版更多的授權時，會獲得更多的彈性。</span><span class="sxs-lookup"><span data-stu-id="841b6-124">The benefits of using OPLs is that you get more flexibility in creating license restrictions than previous versions.</span></span> <span data-ttu-id="841b6-125">此外，OPLs 可哥擴充以容納未來的技術。</span><span class="sxs-lookup"><span data-stu-id="841b6-125">In addition, OPLs are expandable to accommodate future technologies.</span></span> <span data-ttu-id="841b6-126">您可以使用 [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) 介面的方法，在您的應用程式中支援這類授權。</span><span class="sxs-lookup"><span data-stu-id="841b6-126">You can support such licenses in your applications by using the methods of the [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) interface.</span></span>

<span data-ttu-id="841b6-127">若要讀取由指定 OPLs 的授權所保護的檔案，您必須檢查 OPL 是否有想要的動作。</span><span class="sxs-lookup"><span data-stu-id="841b6-127">To read files that are protected by a license that specifies OPLs, you must check the OPL for the desired action.</span></span> <span data-ttu-id="841b6-128">授權中的 OPL 必須允許您的應用程式所使用的輸出技術。</span><span class="sxs-lookup"><span data-stu-id="841b6-128">The output technology your application is using must be allowed by the OPL in the license.</span></span> <span data-ttu-id="841b6-129">例如，某些受保護音訊的授權可能會要求您使用安全音訊路徑來播放。</span><span class="sxs-lookup"><span data-stu-id="841b6-129">For example, some licenses for protected audio may require that you use secure audio path to play it.</span></span>

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a><span data-ttu-id="841b6-130">設定讀取器來評估輸出保護層級</span><span class="sxs-lookup"><span data-stu-id="841b6-130">Configuring the Reader to Evaluate Output Protection Levels</span></span>

<span data-ttu-id="841b6-131">您必須先呼叫 [**IWMDRMReader2：： SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) 方法，並傳遞 **TRUE** 作為 *FEvaluate* 參數，才能檢查 OPLs 中載入的檔案。</span><span class="sxs-lookup"><span data-stu-id="841b6-131">Before you can check OPLs for files loaded in the reader, you must call the [**IWMDRMReader2::SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) method, passing **TRUE** for the *fEvaluate* parameter.</span></span> <span data-ttu-id="841b6-132">如果您沒有呼叫這個方法，您的應用程式就看不到需要 OPLs 的授權。</span><span class="sxs-lookup"><span data-stu-id="841b6-132">If you do not call this method, licenses that require OPLs are not visible to your application.</span></span>

## <a name="evaluating-copy-output-protection-levels"></a><span data-ttu-id="841b6-133">評估複製輸出保護層級</span><span class="sxs-lookup"><span data-stu-id="841b6-133">Evaluating Copy Output Protection Levels</span></span>

<span data-ttu-id="841b6-134">若要取得複製動作的輸出保護層級，請呼叫 [**IWMDRMReader2：： GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) 方法。</span><span class="sxs-lookup"><span data-stu-id="841b6-134">To get output protection levels for the copy action, call the [**IWMDRMReader2::GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) method.</span></span> <span data-ttu-id="841b6-135">您從呼叫收到的資料會儲存在 [**DRM \_ 複製 \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) 結構中。</span><span class="sxs-lookup"><span data-stu-id="841b6-135">The data you receive from the call is stored in a [**DRM\_COPY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) structure.</span></span> <span data-ttu-id="841b6-136">此結構包含基底輸出保護層級，以指定授權中複製動作的最小輸出層級。</span><span class="sxs-lookup"><span data-stu-id="841b6-136">The structure contains a base output protection level, which specifies the minimum output level for the copy action in the license.</span></span> <span data-ttu-id="841b6-137">不過，DRM \_ 複製 \_ OPL 結構也包含兩個技術識別碼清單：一個適用于以較低的 OPL 分級的所允許技術，另一個則適用于評等等於或高於基底 OPL 但受授許可權制的技術。</span><span class="sxs-lookup"><span data-stu-id="841b6-137">However, the DRM\_COPY\_OPL structure also contains two lists of technology identifiers: one for allowed technologies that are rated at a lower OPL than the base, and one for technologies that are rated equal to or higher than the base OPL but that are restricted by the license.</span></span> <span data-ttu-id="841b6-138">您必須檢查包含與排除專案，以確定授權允許您的應用程式所使用的技術。</span><span class="sxs-lookup"><span data-stu-id="841b6-138">You must check the inclusions and exclusions to ensure that the technology your application is using is allowed by the license.</span></span>

## <a name="evaluating-play-output-protection-levels"></a><span data-ttu-id="841b6-139">評估播放輸出保護層級</span><span class="sxs-lookup"><span data-stu-id="841b6-139">Evaluating Play Output Protection Levels</span></span>

<span data-ttu-id="841b6-140">若要取得播放動作的輸出保護層級，請呼叫 [**IWMDRMReader2：： GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) 方法。</span><span class="sxs-lookup"><span data-stu-id="841b6-140">To get output protection levels for the play action, call the [**IWMDRMReader2::GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) method.</span></span> <span data-ttu-id="841b6-141">您從呼叫收到的資料會儲存在 [**DRM \_ PLAY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) 結構中。</span><span class="sxs-lookup"><span data-stu-id="841b6-141">The data you receive from the call is stored in a [**DRM\_PLAY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) structure.</span></span> <span data-ttu-id="841b6-142">結構包含數個其他結構。</span><span class="sxs-lookup"><span data-stu-id="841b6-142">The structure contains several other structures.</span></span> <span data-ttu-id="841b6-143">播放動作的基底輸出保護層級會以 Drm 的 [**\_ 最小 \_ 輸出 \_ 保護 \_ 層級**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels)結構儲存 (**drm \_ play \_ OPL**) 的 **minOPL** 成員，其定義以各種格式播放內容所需的最小 OPL。</span><span class="sxs-lookup"><span data-stu-id="841b6-143">The base output protection levels for the play action are stored in a [**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) structure (the **minOPL** member of **DRM\_PLAY\_OPL**), which defines the minimum OPL required to play content in a variety of formats.</span></span> <span data-ttu-id="841b6-144">您必須檢查成員是否有應用程式傳遞的輸出格式類型。</span><span class="sxs-lookup"><span data-stu-id="841b6-144">You must check the member for the type of output formats that your application delivers.</span></span>

<span data-ttu-id="841b6-145">**DRM \_ PLAY \_ OPL** 結構定義了兩種限制：需要向下取樣，以及允許的影片輸出保護識別碼。</span><span class="sxs-lookup"><span data-stu-id="841b6-145">The **DRM\_PLAY\_OPL** structure defines two kinds of restrictions: required down-sampling and allowed video output protection identifiers.</span></span>

<span data-ttu-id="841b6-146">必要的向下取樣定義為 (**DRM \_ PLAY \_ OPL** 的 **oplIdDownsample** 成員的輸出技術識別碼清單) 這種情況下，只有在內容第一次向下取樣時，才可以接收內容以供播放。</span><span class="sxs-lookup"><span data-stu-id="841b6-146">Required down-sampling is defined as a list of output technology identifiers (the **oplIdDownsample** member of **DRM\_PLAY\_OPL**) that, if used, can receive the content for playback only if the content is first down-sampled to a lower bit rate.</span></span>

<span data-ttu-id="841b6-147">允許的影片輸出保護識別碼會定義為影片輸出技術的清單，其中包含每個的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="841b6-147">Allowed video output protection identifiers are defined as a list of video output technologies with configuration information for each.</span></span>

## <a name="handling-multiple-licenses"></a><span data-ttu-id="841b6-148">處理多個授權</span><span class="sxs-lookup"><span data-stu-id="841b6-148">Handling Multiple Licenses</span></span>

<span data-ttu-id="841b6-149">某些檔案可能會在本機授權存放區中有多個相關聯的授權。</span><span class="sxs-lookup"><span data-stu-id="841b6-149">Some files may have multiple licenses associated with them in the local license store.</span></span> <span data-ttu-id="841b6-150">當您針對正在讀取的檔案評估 OPLs 時，您可以藉由呼叫 [**IWMDRMReader2：： TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) 方法來檢查是否有額外的授權。</span><span class="sxs-lookup"><span data-stu-id="841b6-150">When you evaluate OPLs for a file that you are reading, you can check for additional licenses by calling the [**IWMDRMReader2::TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) method.</span></span> <span data-ttu-id="841b6-151">您應繼續嘗試授權，直到找到允許您想要執行之動作的授權，或直到 TryNextLicense 傳回 DRM \_ S \_ FALSE，這表示沒有其他授權。</span><span class="sxs-lookup"><span data-stu-id="841b6-151">You should continue trying licenses until you find one that allows the action you want to perform or until TryNextLicense returns DRM\_S\_FALSE, which indicates that there are no more licenses.</span></span>

<span data-ttu-id="841b6-152">在某些情況下，檔案可能會有相關聯的授權，需要您的應用程式無法支援的 OPL。</span><span class="sxs-lookup"><span data-stu-id="841b6-152">In some cases, a file might have an associated license that requires an OPL that your application cannot support.</span></span> <span data-ttu-id="841b6-153">在這種情況下，請務必檢查是否有額外的授權，因為可能存在未指定 OPLs 的授權。</span><span class="sxs-lookup"><span data-stu-id="841b6-153">In such a case it is important to check for additional licenses because a license may exist that does not specify OPLs.</span></span>

<span data-ttu-id="841b6-154">**注意** 此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="841b6-154">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="841b6-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="841b6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="841b6-156">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="841b6-156">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="841b6-157">**IWMDRMReader2 介面**</span><span class="sxs-lookup"><span data-stu-id="841b6-157">**IWMDRMReader2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




