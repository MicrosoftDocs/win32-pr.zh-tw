---
description: 裝置傳輸狀態
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: 裝置傳輸狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99ea7c3d6cba8363826c0fdab3cf411f0d68d6e284832a75c02cac3b1eefa770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952947"
---
# <a name="device-transport-state"></a>裝置傳輸狀態

若要取得裝置的目前狀態（例如播放、暫停或停止），請呼叫 [**IAMExtTransport：： get \_ 模式**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) 方法。 方法會抓取指出裝置狀態的常數：



| 值                    | 裝置狀態 |
|--------------------------|--------------|
| ED \_ 模式 \_ 播放           | 播放         |
| ED \_ 模式 \_ 停止           | 停止         |
| ED \_ 模式 \_ 凍結         | 暫停        |
| ED \_ 模式 \_ FF             | 向前快轉 |
| ED \_ 模式 \_ 倒轉            | Rewind       |
| ED \_ 模式 \_ 記錄         | Record       |
| ED \_ 模式 \_ 記錄 \_ 凍結 | 記錄-暫停 |



 

下列程式碼會檢查裝置狀態：


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



