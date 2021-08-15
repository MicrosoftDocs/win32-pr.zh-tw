---
description: 處理影片捕獲中的重新繪製事件
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: 處理影片捕獲中的重新繪製事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433a9897c7c69119eb54d088aff2d22536e20ae43760cc6b4c9430f9a44f6814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999757"
---
# <a name="handling-repaint-events-in-video-capture"></a>處理影片捕獲中的重新繪製事件

如果您在不使用 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面的情況下建立影片捕獲圖形，而且您使用舊的影片轉譯器篩選器來預覽影片，則應該覆寫 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件的預設處理。 查詢 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)介面的篩選 Graph 管理員，然後使用 EC 重新繪製的值來呼叫 [**IMediaEvent：： CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling)方法 \_ ：


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



這可防止可能會損毀您的捕獲檔案的錯誤。 如果使用者涵蓋並暴露預覽視窗，則影片轉譯器篩選器會接收 WM \_ 油漆訊息。 根據預設，影片轉譯器會要求新的框架，而篩選 Graph 管理員會暫停圖形，以提示另一個影片畫面。 如果在圖形寫入檔案時發生這種情況，就會損毀檔案。 覆寫預設的 EC 重新 \_ 繪製行為，可防止轉譯器要求新的框架。

如果您使用的是 **ICaptureGraphBuilder2** 介面，則不需要執行此步驟，因為 Capture Graph Builder 會自動為您執行此步驟。 此外，如果您使用影片混合轉譯器 (VMR) 進行預覽，則不需要此項。 VMR 一律具有最新的可用畫面，因此不會傳送 EC 重新 \_ 繪製事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 



