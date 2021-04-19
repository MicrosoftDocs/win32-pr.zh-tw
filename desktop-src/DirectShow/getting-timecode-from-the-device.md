---
description: 從裝置取得時間碼
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: 從裝置取得時間碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991587"
---
# <a name="getting-timecode-from-the-device"></a>從裝置取得時間碼

當 DV 磁帶現正播放或處於「記錄暫停」模式時，您可以取得 SMPTE 時間碼或絕對曲目編號。 若要這樣做，請呼叫 [**IAMTimecodeReader：： GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) 方法。 這個方法會採用時間 [**碼 \_ 範例**](/windows/win32/api/strmif/ns-strmif-timecode_sample) 結構的指標，其描述時間碼。 在呼叫方法之前，請先初始化結構的 **dwFlags** 成員。 使用「讀取」值 \_ DEVCAP 時間 \_ 碼 \_ 來取出時間碼，或使用值 ed \_ DEVCAP \_ ATN \_ read 來取得絕對的曲目編號。

時間 **碼 \_ 範例** 結構的時間 **碼** 成員是時間碼結構。 當方法傳回時，時間碼結構的 **dwFrames** 成員會包含時間碼或曲目編號。 在時間碼中，時、分、秒和框架會以二進位編碼的十進位 (BCD) 值（格式為 *hhmmssff*）封裝成 DWORD。 使用位元遮罩來將個別值解壓縮。

下列範例會抓取時間碼和曲目編號。


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
