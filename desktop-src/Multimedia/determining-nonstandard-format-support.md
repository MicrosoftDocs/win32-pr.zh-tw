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
ms.openlocfilehash: 30a90d38f7419b6fbdb3de951c0aa2205ccd3dd9ff5366eb1e69eab945220db1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497278"
---
# <a name="determining-nonstandard-format-support"></a>判斷非標準格式支援

若要查看裝置是否支援特定格式 (標準或非標準) ，您可以使用 WAVE [](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) \_ 格式查詢旗標來呼叫 waveOutOpen 函數 \_ 。 下列範例會使用這項技術來判斷波形音訊裝置是否支援指定的格式。


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



這項用於判斷非標準格式支援的技巧也適用于波形音訊輸入裝置。 唯一的差別是使用 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 函式來取代 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) ，以查詢格式支援。

若要判斷系統中的任何 WAVE 音訊裝置是否支援特定的波形音訊資料格式，請使用上述範例中所述的技術，但指定 \_ *uDeviceID* 參數的 WAVE 對應器常數。

 

 