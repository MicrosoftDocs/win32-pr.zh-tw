---
description: 本主題說明如何使用 MFPlay 取得媒體檔案的播放持續時間。
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: 如何取得播放持續時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c715ae82c63006ef8ad375fa9624cbd65ee5516be2d3e3379e5ca58a2fb5166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958338"
---
# <a name="how-to-get-the-playback-duration"></a>如何取得播放持續時間

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

本主題說明如何使用 MFPlay 取得媒體檔案的播放持續時間。

**取得播放持續時間**

1.  呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) 或 [**IMFPMediaPlayer：： CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) 來建立檔案的媒體專案。
2.  呼叫 [**IMFPMediaItem：： GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration)。 指定第一個參數的 **MFP \_ positiontype] \_ 100ns** 。 持續時間會以包含 **大型 \_ 整數** 值的 **PROPVARIANT** 傳回。 持續時間會以 100-毫微秒單位提供。

下列範例顯示步驟2：


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



