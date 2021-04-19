---
title: MCIERR 傳回值
description: MCIERR 傳回值
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows 多媒體，MCIERR 傳回值
- 多媒體、MCIERR 傳回值
- 多媒體參考，MCIERR 傳回值
- 多媒體的參考，MCIERR 傳回值
- MCIERR 傳回值，關於
- mciSendCommand 函式
- mciSendString 函式
- Windows 多媒體，錯誤
- 多媒體，錯誤
- 多媒體參考，錯誤
- 多媒體的參考，錯誤
- 媒體控制介面 (MCI) 、MCIERR 傳回值
- MCI (媒體控制介面) ，MCIERR 傳回值
- MCI 的參考，MCIERR 傳回值
- MCI 參考，MCIERR 傳回值
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967476"
---
# <a name="mcierr-return-values"></a><span data-ttu-id="fbd27-122">MCIERR 傳回值</span><span class="sxs-lookup"><span data-stu-id="fbd27-122">MCIERR Return Values</span></span>

<span data-ttu-id="fbd27-123">如果成功， [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 和 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函數會傳回零;否則，它們會傳回 **DWORD** 值，其中包含低字組中的下列其中一個錯誤值。</span><span class="sxs-lookup"><span data-stu-id="fbd27-123">The [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) and [**mciSendString**](/previous-versions//dd757161(v=vs.85)) functions return zero if they are successful; otherwise, they return a **DWORD** value that contains one of the following error values in the low word.</span></span>

-   [<span data-ttu-id="fbd27-124">一般 MCI 錯誤</span><span class="sxs-lookup"><span data-stu-id="fbd27-124">General MCI Errors</span></span>](general-mci-errors.md)
-   [<span data-ttu-id="fbd27-125">mciSendString 錯誤</span><span class="sxs-lookup"><span data-stu-id="fbd27-125">mciSendString Errors</span></span>](mcisendstring-errors.md)
-   [<span data-ttu-id="fbd27-126">數位影片錯誤</span><span class="sxs-lookup"><span data-stu-id="fbd27-126">Digital-Video Errors</span></span>](digital-video-errors.md)
-   [<span data-ttu-id="fbd27-127">Sequencer 錯誤</span><span class="sxs-lookup"><span data-stu-id="fbd27-127">Sequencer Errors</span></span>](sequencer-errors.md)
-   [<span data-ttu-id="fbd27-128">波形-音訊錯誤</span><span class="sxs-lookup"><span data-stu-id="fbd27-128">Waveform-Audio Errors</span></span>](waveform-audio-errors.md)

<span data-ttu-id="fbd27-129">您可以藉由將傳回值傳遞至 [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) 函式，來取得個別傳回值的描述。</span><span class="sxs-lookup"><span data-stu-id="fbd27-129">You can obtain a description of individual return values by passing the return values to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function.</span></span>

 

 