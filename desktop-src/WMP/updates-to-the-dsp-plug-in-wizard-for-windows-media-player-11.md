---
title: Windows Media Player 11 的 DSP 外掛程式嚮導更新
description: Windows Media Player 11 的 DSP 外掛程式嚮導更新
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Windows Media Player 外掛程式，外掛程式嚮導
- 外掛程式、外掛程式嚮導
- 數位信號處理外掛程式，外掛程式嚮導
- DSP 外掛程式，外掛程式嚮導
- 外掛程式嚮導
- Visual Studio，DSP 外掛程式 wizard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374459"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a><span data-ttu-id="6bba9-109">Windows Media Player 11 的 DSP 外掛程式嚮導更新</span><span class="sxs-lookup"><span data-stu-id="6bba9-109">Updates to the DSP Plug-in Wizard for Windows Media Player 11</span></span>

<span data-ttu-id="6bba9-110">Windows Media Player 11 SDK 引進了下列對 DSP 外掛程式 wizard 的變更：</span><span class="sxs-lookup"><span data-stu-id="6bba9-110">The Windows Media Player 11 SDK introduces the following changes to the DSP plug-in wizard:</span></span>

-   <span data-ttu-id="6bba9-111">外掛程式會將執行緒模型註冊為「兩者」。</span><span class="sxs-lookup"><span data-stu-id="6bba9-111">Plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="6bba9-112">這可讓外掛程式在 Windows Vista 上的媒體基礎管線中執行。</span><span class="sxs-lookup"><span data-stu-id="6bba9-112">This enables the plug-in to run in the Media Foundation pipeline on Windows Vista.</span></span> <span data-ttu-id="6bba9-113">請參閱 *專案名稱*.rgs 檔。</span><span class="sxs-lookup"><span data-stu-id="6bba9-113">See the *projectname*.rgs file.</span></span>

    -   <span data-ttu-id="6bba9-114">音訊 DSP 外掛程式支援下列兩種額外的格式：</span><span class="sxs-lookup"><span data-stu-id="6bba9-114">Audio DSP plug-ins have support for the following two additional formats:</span></span>

    <!-- -->

    -   <span data-ttu-id="6bba9-115">WAVE \_ 格式 \_ IEEE \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="6bba9-115">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
    -   <span data-ttu-id="6bba9-116">WAVE \_ 格式可延伸 \_ 的 subformat KSDATAFORMAT \_ 子類型 \_ IEEE \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="6bba9-116">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

    <span data-ttu-id="6bba9-117">請參閱 *專案名稱*.cpp 檔案。</span><span class="sxs-lookup"><span data-stu-id="6bba9-117">See the *projectname*.cpp file.</span></span>

    1.  <span data-ttu-id="6bba9-118">影片 DSP 外掛程式支援 NV12 影片格式。</span><span class="sxs-lookup"><span data-stu-id="6bba9-118">Video DSP plug-ins have support for the NV12 video format.</span></span>
    2.  <span data-ttu-id="6bba9-119">外掛程式會使用新的外掛程式類型，對 [IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) 和 [IWMPMediaPluginRegistrar：： WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) 進行額外的呼叫： WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC。</span><span class="sxs-lookup"><span data-stu-id="6bba9-119">Plug-ins make additional calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC.</span></span> <span data-ttu-id="6bba9-120">請參閱專案的 *projectnamedll*.cpp 檔案。</span><span class="sxs-lookup"><span data-stu-id="6bba9-120">See the project's *projectnamedll*.cpp file.</span></span>
    3.  <span data-ttu-id="6bba9-121">每個方案中的其他專案會為屬性頁面設定自訂介面建立 proxy/存根 DLL。</span><span class="sxs-lookup"><span data-stu-id="6bba9-121">An additional project in each solution creates a proxy/stub DLL for the property page settings custom interface.</span></span> <span data-ttu-id="6bba9-122">請參閱 *projectnamePS* 專案。</span><span class="sxs-lookup"><span data-stu-id="6bba9-122">See the *projectnamePS* project.</span></span>
    4.  <span data-ttu-id="6bba9-123">對已被取代之方法的呼叫已變更為使用最新版本。</span><span class="sxs-lookup"><span data-stu-id="6bba9-123">Calls to deprecated methods have been changed to use the newest versions.</span></span>
    5.  <span data-ttu-id="6bba9-124">您可以藉由執行 **IMFTransform** 來藉由執行 **IMediaObject** 和 MFT，來產生雙重模式外掛程式，以做為一。</span><span class="sxs-lookup"><span data-stu-id="6bba9-124">The wizard can generate a dual-mode plug-in that functions both as a DMO, by implementing **IMediaObject**, and as an MFT, by implementing **IMFTransform**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bba9-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="6bba9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bba9-126">**DSP 外掛程式嚮導**</span><span class="sxs-lookup"><span data-stu-id="6bba9-126">**DSP Plug-in Wizard**</span></span>](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




