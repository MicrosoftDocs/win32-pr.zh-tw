---
description: DV 攝影機的外部裝置介面
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: DV 攝影機的外部裝置介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e7106ec6e9b744da0d1f71958aeb895ec8df1a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909796"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a>DV 攝影機的外部裝置介面

[WDM 影片捕獲](wdm-video-capture-filter.md)篩選器會公開三個介面來控制攝影機。



| 標籤 | 值 |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | 外部裝置控制的基底介面。 |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | 控制 VCR 函數。                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | 從裝置讀取時間碼。                 |



 

> [!Note]  
> 若要搭配使用這些介面與 MSDV 攝影機驅動程式，請在您的專案中包含標頭檔 XPrtDefs。

 

在您選取 capture 裝置並建立 capture 篩選器的實例之後，請查詢這些介面的篩選。 下列範例會宣告保存介面指標的自訂結構，以及指定每個介面可用性的布林值：


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



