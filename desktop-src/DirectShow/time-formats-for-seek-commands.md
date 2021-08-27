---
description: 搜尋命令的時間格式
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: 搜尋命令的時間格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e585a7dda12b40e7f501e51aff6ffed50d647066f03804c82e5ffa236f8623a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078718"
---
# <a name="time-formats-for-seek-commands"></a>搜尋命令的時間格式

**IMediaSeeking** 介面中的許多方法都具有表示位置值的參數，例如目前的位置或停止位置。 根據預設，這些參數會以100毫微秒的單位來表示，也稱為參考時間。 任何可以搜尋的篩選準則都必須支援依參考時間進行搜尋。 某些篩選器也可以使用其他時間單位來搜尋，例如搜尋特定的框架編號，或搜尋資料流程內的指定位元組位移。 每個時間單位都稱為時間格式，而且是由全域唯一識別碼 (GUID) 所定義。 如需 DirectShow 所定義的時間格式清單，請參閱 [**時間格式 guid**](time-format-guids.md)。 協力廠商也可以定義自訂時間格式的 Guid。

若要判斷目前在篩選圖形中的篩選是否支援特定時間格式，請呼叫 [**IMediaSeeking：： IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) 方法。 如果支援格式，則方法會傳回 S \_ OK。 否則，它會傳回 \_ FALSE 或錯誤碼。 如果支援格式，您可以藉由呼叫 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 方法切換為該格式。 如果 **SetTimeFormat** 方法成功，則會使用新的時間格式來表示後續的搜尋命令。

下列範例會檢查圖形是否支援依框架編號搜尋。 如果是，則會搜尋框架編號20：


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



請注意，時間格式只適用于搜尋命令。 它們不會影響圖形播放或其他動作。

 

 



