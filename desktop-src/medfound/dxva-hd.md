---
description: Microsoft DirectX Video 加速 High Definition (DXVA-HD) 是用於硬體加速影片處理的 API。
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40e23d6e91f576f062c52a0f58d0bfe1f769ad3879581b01386333266cb0553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958648"
---
# <a name="dxva-hd"></a>DXVA-HD

Microsoft DirectX Video 加速 High Definition (DXVA-HD) 是用於硬體加速影片處理的 API。 DXVA-HD 使用 GPU 來執行去交錯、合成和色彩空間轉換等功能。

DXVA-HD 類似于 [DXVA 影片處理](dxva-video-processing.md) (DXVA-VP) ，但提供增強的功能和更簡單的處理模型。 藉由提供更有彈性的組合模型，DXVA-HD 設計為支援新一代的 HD 光學格式和廣播標準。

DXVA-HD API 需要 WDDM 顯示器驅動程式，以支援 DXVA-HD 設備磁碟機介面 (的 DDI) 或外掛程式軟體處理器。

-   [超越 DXVA 的改進-VP](#improvements-over-dxva-vp)
-   [相關主題](#related-topics)

## <a name="improvements-over-dxva-vp"></a>超越 DXVA 的改進-VP

DXVA-HD 擴展 DXVA （VP）所提供的一組功能。 增強功能包括：

-   RGB 和 YUV 混合。 任何資料流程可以是 RGB 或 YUV。 主要資料流程與子串流之間已不再有所差異。
-   多個資料流程的去交錯。 任何資料流程可以是漸進式或交錯式。 此外，步調和畫面播放速率可能會因某個輸入資料流程而異。
-   RGB 背景色彩。 先前只支援 YUV 的背景色彩。
-   Luma 金鑰。 啟用 luma 金鑰時，落在指定範圍內的 luma 值會變成透明。
-   在交錯模式之間動態切換。

DXVA-HD 也會定義一些驅動程式可支援的先進功能。 不過，應用程式不應該假設所有驅動程式都支援這些功能。 先進的功能包括：

-   反向電視電視 (例如，60i 至 24p) 。
-   畫面播放速率轉換 (例如，24p 至 120p) 。
-   Alpha 填滿模式。
-   減少雜訊和邊緣增強篩選。
-   Anamorphic 非線性調整。
-   外延 YCbCr (xvYCC) 。

此章節包含下列主題。

-   [建立 DXVA-HD 視頻處理器](creating-a-dxva-hd-video-processor.md)
-   [檢查支援的 DXVA-HD 格式](checking-supported-dxva-hd-formats.md)
-   [建立 DXVA-HD 影片表面](creating-dxva-hd-video-surfaces.md)
-   [設定 DXVA-HD 狀態](setting-dxva-hd-states.md)
-   [執行 DXVA-HD Array.blit](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA-HD 範例](dxva-hd-sample.md)
</dt> </dl>

 

 



