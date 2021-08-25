---
description: 處理影片轉譯器的格式變更
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: 處理影片轉譯器的格式變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1dd0ec2f87a8604d3b03aa6c2f334161d218f4d7fb45c76aad1015f071d947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905298"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>處理影片轉譯器的格式變更

本節說明「解碼器篩選準則」或「轉換」篩選器如何處理來自影片轉譯器的格式變更。

**影片轉譯器篩選**

當舊的 [影片](video-renderer-filter.md) 轉譯器篩選連接時，需要符合主要監視器顯示格式的 RGB 格式。 這可讓它在 DirectDraw 無法使用的情況下，使用 GDI 來呈現。 播放開始時，影片轉譯器可能會切換到 DirectDraw 相容的格式。 為了 verfify 上游篩選是否可支援新的格式，影片轉譯器會在上游篩選器的輸出釘選上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。 如果上游篩選器接受新的格式， **QueryAccept** 方法會傳回 S \_ OK。 影片轉譯器會切換格式，方法是將具有新格式的媒體類型附加至其配置器所傳回的下一個媒體範例。 上游篩選器應該在每個範例上呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) ，以檢查格式變更。 影片轉譯器可能會在串流期間的任何時間，從原始格式和新格式來回切換。 它不會在第一次格式變更之後呼叫 **QueryAccept** 。 上游篩選器接受新的格式之後，就必須能夠來回切換。

上游篩選器會從 QueryAccept 傳回 FALSE，以拒絕格式變更 \_ 。  在此情況下，影片轉譯器會繼續使用具有原始格式的 GDI。

**影片混合轉譯器篩選**

影片混合轉譯器篩選器 (VMR-7 和 VMR-9) 將會連接到系統上圖形硬體所支援的任何格式。 VMR-7 一律會使用 DirectDraw 進行轉譯，並且在上游篩選連接時配置基礎 DirectDraw 表面。 VMR-9 一律會使用 Direct3D 進行轉譯，並且在上游篩選連接時配置基礎 Direct3D 表面。

圖形硬體可能需要比影像寬度更大的 surface stride。 在此情況下，VMR 會藉由呼叫 **QueryAccept** 來要求新的格式。 它會以影片格式報告 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)的 **biWidth** 成員中的表面 stride。 如果上游篩選不會 \_ 從 **QueryAccept** 傳回 S OK，則 VMR 會拒絕格式，並嘗試使用上游篩選器所通告的下一個格式來進行連接。 VMR 會將具有新格式的媒體類型附加至第一個媒體範例。 在第一個範例之後，格式會維持不變;當圖形正在執行時，VMR 不會切換格式。

**增強的影片呈現 (EVR)**

EVR 一律使用 Direct3D 來呈現。 如果需要較大的介面 stride，EVR 會使用與 VMR 相同的 **QueryAccept** 機制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[QueryAccept (上游) ](queryaccept--upstream.md)
</dt> </dl>

 

 



