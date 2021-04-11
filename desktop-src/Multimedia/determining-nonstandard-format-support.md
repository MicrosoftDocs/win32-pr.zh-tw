---
title: 判斷非標準格式支援
description: 判斷非標準格式支援
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- 波形音訊、非標準格式支援
- 輔助音訊、非標準格式支援
- 波形音訊、標準格式支援
- 輔助音訊、標準格式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0933a82ca8da53c89e1cb8b7d32b40dc89ae0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023388"
---
# <a name="determining-nonstandard-format-support"></a><span data-ttu-id="c4346-107">判斷非標準格式支援</span><span class="sxs-lookup"><span data-stu-id="c4346-107">Determining Nonstandard Format Support</span></span>

<span data-ttu-id="c4346-108">若要查看裝置是否支援特定格式 (標準或非標準) ，您可以使用 WAVE [](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) \_ 格式查詢旗標來呼叫 waveOutOpen 函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c4346-108">To see whether a device supports a particular format (standard or nonstandard), you can call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function with the WAVE\_FORMAT\_QUERY flag.</span></span> <span data-ttu-id="c4346-109">下列範例會使用這項技術來判斷波形音訊裝置是否支援指定的格式。</span><span class="sxs-lookup"><span data-stu-id="c4346-109">The following example uses this technique to determine whether a waveform-audio device supports a specified format.</span></span>


```C++
// Determines whether the specified waveform-audio output device 
// supports a specified waveform-audio format. Returns 
// MMSYSERR_NOERROR if the format is supported, WAVEERR_BADFORMAT if 
// the format is not supported, and one of the other MMSYSERR_ error 
// codes if there are other errors encountered in opening the 
// specified waveform-audio device. 
 
MMRESULT IsFormatSupported(LPWAVEFORMATEX pwfx, UINT uDeviceID) 
{ 
    return (waveOutOpen( 
        NULL,                 // ptr can be NULL for query 
        uDeviceID,            // the device identifier 
        pwfx,                 // defines requested format 
        NULL,                 // no callback 
        NULL,                 // no instance data 
        WAVE_FORMAT_QUERY));  // query only, do not open device 
} 
```



<span data-ttu-id="c4346-110">這項用於判斷非標準格式支援的技巧也適用于波形音訊輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="c4346-110">This technique for determining nonstandard format support also applies to waveform-audio input devices.</span></span> <span data-ttu-id="c4346-111">唯一的差別是使用 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 函式來取代 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) ，以查詢格式支援。</span><span class="sxs-lookup"><span data-stu-id="c4346-111">The only difference is that the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function is used in place of [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) to query for format support.</span></span>

<span data-ttu-id="c4346-112">若要判斷系統中的任何 WAVE 音訊裝置是否支援特定的波形音訊資料格式，請使用上述範例中所述的技術，但指定 \_ *uDeviceID* 參數的 WAVE 對應器常數。</span><span class="sxs-lookup"><span data-stu-id="c4346-112">To determine whether a particular waveform-audio data format is supported by any of the waveform-audio devices in a system, use the technique illustrated in the previous example, but specify the WAVE\_MAPPER constant for the *uDeviceID* parameter.</span></span>

 

 