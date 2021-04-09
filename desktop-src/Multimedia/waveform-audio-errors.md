---
title: Waveform-Audio 錯誤
description: Waveform-Audio 錯誤
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- MCIERR 傳回值、波形-音訊錯誤
- 多媒體參考、波形-音訊錯誤
- 多媒體的參考，波形-音訊錯誤
- 媒體控制介面 (MCI) 、波形-音訊錯誤
- MCI (媒體控制介面) 、波形-音訊錯誤
- MCI 的參考、波形-音訊錯誤
- MCI 參考、波形-音訊錯誤
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
- 波形-音訊錯誤
- MCI 波形-音訊錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021043"
---
# <a name="waveform-audio-errors"></a><span data-ttu-id="22af0-116">Waveform-Audio 錯誤</span><span class="sxs-lookup"><span data-stu-id="22af0-116">Waveform-Audio Errors</span></span>

<span data-ttu-id="22af0-117">下列額外的傳回值是針對 MCI 波形-音訊裝置所定義：</span><span class="sxs-lookup"><span data-stu-id="22af0-117">The following additional return values are defined for MCI waveform-audio devices:</span></span>



| <span data-ttu-id="22af0-118">值</span><span class="sxs-lookup"><span data-stu-id="22af0-118">Value</span></span>                             | <span data-ttu-id="22af0-119">意義</span><span class="sxs-lookup"><span data-stu-id="22af0-119">Meaning</span></span>                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22af0-120">MCIERR \_ WAVE \_ INPUTSINUSE</span><span class="sxs-lookup"><span data-stu-id="22af0-120">MCIERR\_WAVE\_INPUTSINUSE</span></span>         | <span data-ttu-id="22af0-121">可以用目前格式記錄檔案的所有波形裝置都在使用中。</span><span class="sxs-lookup"><span data-stu-id="22af0-121">All waveform devices that can record files in the current format are in use.</span></span> <span data-ttu-id="22af0-122">等到其中一個裝置是免費的，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="22af0-122">Wait until one of these devices is free; then, try again.</span></span>                              |
| <span data-ttu-id="22af0-123">MCIERR \_ WAVE \_ INPUTSUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="22af0-123">MCIERR\_WAVE\_INPUTSUNSUITABLE</span></span>    | <span data-ttu-id="22af0-124">沒有任何已安裝的波形裝置可以記錄目前格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="22af0-124">No installed waveform device can record files in the current format.</span></span> <span data-ttu-id="22af0-125">使用主控台的 [驅動程式] 選項來安裝適當的波形錄製裝置。</span><span class="sxs-lookup"><span data-stu-id="22af0-125">Use the Drivers option from the Control Panel to install a suitable waveform recording device.</span></span> |
| <span data-ttu-id="22af0-126">MCIERR \_ WAVE \_ INPUTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="22af0-126">MCIERR\_WAVE\_INPUTUNSPECIFIED</span></span>    | <span data-ttu-id="22af0-127">您可以指定任何相容的波形錄製裝置。</span><span class="sxs-lookup"><span data-stu-id="22af0-127">You can specify any compatible waveform recording device.</span></span>                                                                                                           |
| <span data-ttu-id="22af0-128">MCIERR \_ WAVE \_ OUTPUTSINUSE</span><span class="sxs-lookup"><span data-stu-id="22af0-128">MCIERR\_WAVE\_OUTPUTSINUSE</span></span>        | <span data-ttu-id="22af0-129">所有可播放目前格式之檔案的波形裝置皆為使用中。</span><span class="sxs-lookup"><span data-stu-id="22af0-129">All waveform devices that can play files in the current format are in use.</span></span> <span data-ttu-id="22af0-130">等到其中一個裝置是免費的，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="22af0-130">Wait until one of these devices is free; then, try again.</span></span>                                |
| <span data-ttu-id="22af0-131">MCIERR \_ WAVE \_ OUTPUTSUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="22af0-131">MCIERR\_WAVE\_OUTPUTSUNSUITABLE</span></span>   | <span data-ttu-id="22af0-132">沒有任何已安裝的波形裝置可以播放目前格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="22af0-132">No installed waveform device can play files in the current format.</span></span> <span data-ttu-id="22af0-133">使用主控台的 [驅動程式] 選項來安裝適當的波形裝置。</span><span class="sxs-lookup"><span data-stu-id="22af0-133">Use the Drivers option from the Control Panel to install a suitable waveform device.</span></span>             |
| <span data-ttu-id="22af0-134">MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="22af0-134">MCIERR\_WAVE\_OUTPUTUNSPECIFIED</span></span>   | <span data-ttu-id="22af0-135">您可以指定任何相容的波形播放裝置。</span><span class="sxs-lookup"><span data-stu-id="22af0-135">You can specify any compatible waveform playback device.</span></span>                                                                                                            |
| <span data-ttu-id="22af0-136">MCIERR \_ WAVE \_ SETINPUTINUSE</span><span class="sxs-lookup"><span data-stu-id="22af0-136">MCIERR\_WAVE\_SETINPUTINUSE</span></span>       | <span data-ttu-id="22af0-137">目前的波形裝置正在使用中。</span><span class="sxs-lookup"><span data-stu-id="22af0-137">The current waveform device is in use.</span></span> <span data-ttu-id="22af0-138">等待裝置免費;然後，再試一次設定裝置以進行錄製。</span><span class="sxs-lookup"><span data-stu-id="22af0-138">Wait until the device is free; then, try again to set the device for recording.</span></span>                                              |
| <span data-ttu-id="22af0-139">MCIERR \_ WAVE \_ SETINPUTUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="22af0-139">MCIERR\_WAVE\_SETINPUTUNSUITABLE</span></span>  | <span data-ttu-id="22af0-140">您用來錄製波形的裝置無法辨識資料格式。</span><span class="sxs-lookup"><span data-stu-id="22af0-140">The device you are using to record a waveform cannot recognize the data format.</span></span>                                                                                     |
| <span data-ttu-id="22af0-141">MCIERR \_ WAVE \_ SETOUTPUTINUSE</span><span class="sxs-lookup"><span data-stu-id="22af0-141">MCIERR\_WAVE\_SETOUTPUTINUSE</span></span>      | <span data-ttu-id="22af0-142">目前的波形裝置正在使用中。</span><span class="sxs-lookup"><span data-stu-id="22af0-142">The current waveform device is in use.</span></span> <span data-ttu-id="22af0-143">等待裝置免費;然後，再試一次設定裝置以進行播放。</span><span class="sxs-lookup"><span data-stu-id="22af0-143">Wait until the device is free; then, try again to set the device for playback.</span></span>                                               |
| <span data-ttu-id="22af0-144">MCIERR \_ WAVE \_ SETOUTPUTUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="22af0-144">MCIERR\_WAVE\_SETOUTPUTUNSUITABLE</span></span> | <span data-ttu-id="22af0-145">您用來播放波形的裝置無法辨識資料格式。</span><span class="sxs-lookup"><span data-stu-id="22af0-145">The device you are using to playback a waveform cannot recognize the data format.</span></span>                                                                                   |



 

 

 




