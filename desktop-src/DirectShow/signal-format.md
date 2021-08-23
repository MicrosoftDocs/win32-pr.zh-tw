---
description: 信號格式
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: 信號格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66add7467f2f497985094c603aaea83b55967f6b2c07eba4cacde080503ef2e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583178"
---
# <a name="signal-format"></a>信號格式

DV 攝像機的信號格式可以是 NTSC、PAL、標準或長時間播放。

**MSDV 驅動程式**

若要從 MSDV 驅動程式取得輸入信號格式，請呼叫 [**IAMExtTransport：： GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) 方法並傳入 ED \_ TRANSBASIC \_ 輸入 \_ 信號旗標。 方法會傳回定義的常數，表示格式。

下列程式碼會檢查信號格式，並使用此值來計算每個畫面格的平均時間。 變數模式會接收信號格式常數。


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



若要取得輸出信號格式，請使用 ED \_ TRANSBASIC \_ 輸出信號旗標來呼叫相同的方法 \_ 。

**UVC 驅動程式**

若要從 UVC 驅動程式取得輸入或輸出信號格式，請在 pin 上呼叫 [**IAMStreamConfig：： >iformatprovider.getformat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) ，並檢查影片格式區塊。 針對 UVC 裝置 (，上述範例中所示的程式碼通常會傳回 ED \_ TRANSBASIC \_ 信號 \_ 未知，因此不可靠。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



