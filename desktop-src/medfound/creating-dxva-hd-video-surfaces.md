---
description: 建立 DXVA-HD 影片表面
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: 建立 DXVA-HD 影片表面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40058a02c179a8f9f0690eea9cce777bdd0563d5d27b36ddcb3d34f8fff8a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829048"
---
# <a name="creating-dxva-hd-video-surfaces"></a>建立 DXVA-HD 影片表面

應用程式必須建立一或多個 Direct3D 介面，以用於輸入畫面。 這些必須配置於 [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)結構的 **InputPool** 成員所指定的記憶體集區中。 您可以使用下列介面類別型：

-   藉由呼叫 [**IDXVAHD \_ Device：： CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) 並指定 **DXVAHD \_ 介面 \_ 類型 \_ 影片 \_ 輸入** 或 DXVAHD 介面類別型的 **影片 \_ \_ \_ \_ 輸入 \_ 私人** 介面類別型所建立的視頻界面。 此介面類別型相當於非畫面的一般表面。
-   藉由呼叫 [**IDirectXVideoAccelerationService：： CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) 並指定 **DXVA2 \_ VideoDecoderRenderTarget** 介面型別所建立的「解碼器呈現目標介面」。 此介面類別型用於 DXVA 解碼。
-   純螢幕表面。

下列程式碼顯示如何使用 [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface)來配置視頻界面：


```C++
    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



