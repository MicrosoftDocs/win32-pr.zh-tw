---
description: VMR 系統需求
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: VMR 系統需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d03d5a195f675b911dff85860592c3ec3b5a39ec4f65a51cdc594bc8744906
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632998"
---
# <a name="vmr-system-requirements"></a>VMR 系統需求

VMR 會以獨佔方式使用電腦顯示配接器的圖形處理功能;VMR 不會使用主機處理器來執行任何的影片混色或轉譯，因為這樣做會大幅影響畫面播放速率和所顯示影片的品質。 當您利用 VMR 所提供的新功能時（特別是多個影片串流及/或應用程式影像的混合），所取得的整體效能將高度依賴電腦上所使用之圖形配接器的功能。 與 VMR 搭配運作的圖形配接器，具有下列內建的硬體支援：

-   支援 YUV 和「非乘2」 Direct3D 材質表面。
-   從 YUV StretchBlt 至 RGB DirectDraw 表面的能力。
-   如果有多個影片串流要混合在一起，則至少有16MB 的視訊記憶體。 實際所需的記憶體數量取決於影片串流的影像大小，以及所使用的顯示模式解析度。
-   支援 RGB 重迭或 blend 至 YUV 重迭表面的能力。
-   硬體加速影片 (支援 DirectX Video 加速) 解碼。
-   高圖元填滿率。

> [!Note]  
> VMR 要求系統監視器必須設定至少16位的色彩深度。 如果已針對256色彩設定監視，則無法將 VMR 置於執行狀態。 此外，當顯示器設為每圖元24位時，某些視訊卡無法執行 Direct3D 作業。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於影片混合轉譯](about-the-video-mixing-render.md)
</dt> </dl>

 

 



