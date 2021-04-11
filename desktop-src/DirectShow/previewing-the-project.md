---
description: 預覽專案
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: 預覽專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935927"
---
# <a name="previewing-the-project"></a>預覽專案

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

若要預覽專案，您需要一個稱為轉譯 *引擎* 的元件，該元件會從時間軸建立 DirectShow 篩選圖形。 篩選圖形是實際呈現專案的專案。 您可以使用轉譯引擎來預覽專案或寫入最終輸出檔。

本文不會詳細說明轉譯引擎。 針對預覽，您只需要幾個方法呼叫。 您可以在轉譯 [專案](rendering-a-project.md)中找到更詳盡的討論，包括如何寫入輸出檔。 下列程式碼範例顯示如何建立預覽圖形。


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



使用 **CoCreateInstance** 函數建立轉譯引擎。 然後，在轉譯引擎的 [**IRenderEngine**](irenderengine.md) 介面上呼叫下列方法：

-   [**SetTimelineObject**](irenderengine-settimelineobject.md)。 指定要使用的時間軸。
-   [**ConnectFrontEnd**](irenderengine-connectfrontend.md)。 建立部分篩選圖形，其中每個群組的輸出釘選在時間軸中。
-   [**RenderOutputPins**](irenderengine-renderoutputpins.md)。 將每個輸出圖釘連接至影片或音訊轉譯器，以完成預覽圖形。

建立圖表之後，您可以執行圖形來預覽專案，就像使用任何 DirectShow 篩選圖形一樣。 首先，藉由呼叫 [**IRenderEngine：： GetFilterGraph**](irenderengine-getfiltergraph.md) 方法來取得篩選圖形的指標。


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



查詢 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 和 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 介面的篩選圖形。 您可以使用這兩個介面來執行圖形，並等候播放完成。 如需如何使用這些介面的說明，請參閱 [如何播放](how-to-play-a-file.md) 檔案和 [回應事件](responding-to-events.md)。 下列程式碼顯示使用這些介面的一種方式。


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



此範例中的程式碼會封鎖程式執行，直到播放完成為止，因為 [**IMediaEvent：： WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) 方法呼叫中有無限的參數。 但是，如果在播放期間發生錯誤，可能會導致程式停止回應。 在實際的應用程式中，使用訊息迴圈來等候播放完成。 此外，也建議您為使用者提供中斷播放的方式。

當您完成使用轉譯引擎時，請一律呼叫 [**IRenderEngine：： ScrapIt**](irenderengine-scrapit.md) 方法。 這個方法會刪除篩選圖形，並釋放轉譯引擎所持有的任何資源。


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[載入和預覽專案](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



