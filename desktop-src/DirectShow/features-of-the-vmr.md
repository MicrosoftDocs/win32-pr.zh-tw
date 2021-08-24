---
description: VMR 的功能
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: VMR 的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c78fc34be3097beedb73ac3989bc468cff0851143355902e3236f672797a83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819550"
---
# <a name="features-of-the-vmr"></a>VMR 的功能

影片混合轉譯器 7 (VMR-7) 支援下列新功能：

-   使用 Direct3D 硬體裝置的 Alpha 混合功能，來真正混合多個視頻串流。
-   能夠插入您自己的複合元件，以在多個進入 VMR 的影片資料流程之間執行效果和轉換。
-   真正無視窗呈現。 您不再需要讓影片播放視窗成為應用程式視窗的子系，以便包含影片播放。 VMR 的新無視窗轉譯模式，可讓應用程式輕鬆地在任何視窗內裝載影片播放，而不需要將視窗訊息轉寄到轉譯器特定的處理常式。
-   新的 renderless 播放模式，在此模式中，應用程式可以提供自己的配置器元件，以便在螢幕上顯示已解碼的影片影像之前取得其存取權。
-   改進支援配備多個監視器的電腦。
-   支援 Microsoft 的新 DirectX Video 加速架構。
-   支援在多個 windows 上同時播放高品質的影片。
-   支援 DirectDraw 獨佔模式
-   100% 與現有應用程式的回溯相容性。
-   支援框架逐步執行，以及可靠的方式來捕捉目前顯示的影像。
-   應用程式能輕鬆地將自己的靜態影像資料（例如頻道標誌或 UI 元件）與影片一起以無閃爍的方式)  (。

VMR-9 支援以上所列的所有功能，以及：

-   使用 Direct3D Api （例如圖元著色器）直接處理影片資料的能力。
-   改進支援交錯式影片內容。
-   支援 DirectX 支援的任何平臺。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於影片混合轉譯](about-the-video-mixing-render.md)
</dt> </dl>

 

 



