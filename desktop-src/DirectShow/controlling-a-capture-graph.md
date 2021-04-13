---
description: 控制捕捉圖形
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: 控制捕捉圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6366645f14822a770b828e59b2201e378a0e1e8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510169"
---
# <a name="controlling-a-capture-graph"></a>控制捕捉圖形

篩選圖形管理員的 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 介面具有執行、停止和暫停整個圖形的方法。 但是，如果篩選圖形具有 capture 和 preview 資料流程，您可能會想要獨立控制兩個數據流。 例如，您可能想要預覽影片而不加以捕捉。 您可以透過 [**ICaptureGraphBuilder2：： ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) 方法來執行此動作。

> [!Note]  
> 當捕捉到 Advanced 系統格式 (ASF) 檔案時，此方法無法運作。

 

控制 Capture 資料流程

下列程式碼會將影片捕獲串流設定為執行四秒，並在圖形執行後一秒啟動：


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



第一個參數會指定要控制的資料流程，做為釘選類別 GUID。 第二個參數會提供媒體類型。 第三個參數是 capture 篩選器的指標。 若要控制圖形中的所有 capture 資料流程，請將第二個和第三個參數設定為 **Null**。

接下來的兩個參數會定義資料流程的開始和停止時間（相對於圖形開始執行的時間）。 呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 以執行圖形。 在您執行圖形之前， **ControlStream** 方法不會有任何作用。 如果圖形已在執行中，則設定會立即生效。

最後兩個參數是用來在資料流程啟動和停止時取得事件通知。 針對您使用這個方法所控制的每個資料流程，篩選圖形都會傳送一組事件：在資料流程啟動時 [**開始使用 ec \_ stream \_ \_ control**](ec-stream-control-started.md) ，而當資料流程停止時，則會 [**\_ \_ \_ 停止 ec 資料流程**](ec-stream-control-stopped.md) 控制。 **WStartCookie** 和 **wStopCookie** 的值會當做第二個事件參數使用。 因此，start 事件中的 *lParam2* 等於 **wStartCookie**，而 Stop 事件中的 *lParam2* 等於 **wStopCookie**。 下列程式碼顯示如何取得這些事件：


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



**ControlStream** 方法會定義一些開始和停止時間的特殊值。



|             |                                        |                                    |
|-------------|----------------------------------------|------------------------------------|
|             | 開始                                  | Stop                               |
| MAXLONGLONG | 永遠不會啟動此資料流程。               | 除非圖形停止，否則請勿停止。 |
| **NULL**    | 在圖形執行時立即啟動。 | 立即停止。                  |



 

例如，下列程式碼會立即停止 capture 資料流程：


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



雖然您可以停止 capture 資料流程並于稍後重新開機，但這會在時間戳記中產生間距。 在播放時，根據檔案格式) ，影片會顯示在間距 (期間會停止。

控制預覽資料流程

若要控制預覽 pin，請呼叫 **ControlStream** ，但設定第一個參數來釘選 \_ 類別目錄 \_ 預覽。 其運作方式就像是釘選 \_ 類別 \_ 捕捉一樣，不同的是，您無法使用參考時間來指定開始和停止，因為預覽畫面沒有時間戳記。 因此，您必須使用 **Null** 或 MAXLONGLONG。 使用 **Null** 來啟動預覽資料流程：


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



使用 MAXLONGLONG 來停止預覽資料流程：


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



預覽資料流程是否來自 capture 篩選器上的預覽 pin，或來自智慧型指標篩選器，並不重要。 **ControlStream** 方法的運作方式有兩種。

不過，若為影片埠 pin，方法將會失敗。 在這種情況下，另一種方法是隱藏影片視窗。 查詢圖表以取得 **IVideoWindow**，並使用 [ [**IVideoWindow：:p] \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) 顯示或隱藏視窗。


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



此外，如果您在執行圖形之前呼叫 [**IVideoWindow：:p \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) ] OAFALSE 會顯示值，則影片轉譯器篩選會隱藏視窗，直到您另外指定為止。 根據預設，影片轉譯器會在您執行圖形時顯示視窗。

關於資料流程控制的備註

Pin 的預設行為是在圖形執行時傳遞範例。 例如，假設您使用 PIN 類別捕獲來呼叫 **ControlStream** ， \_ \_ 而不是使用 pin \_ 類別 \_ 預覽。 當您執行圖形時，預覽資料流程會立即執行，而 capture 資料流程則會在您于 **ControlStream** 中指定的任何時間執行。

如果您要捕捉一個以上的資料流程，並將它們傳送至 mux 篩選器（例如，如果您要將音訊和影片捕獲到 AVI 檔案），您應該一次控制兩個數據流。 否則，mux 篩選器可能會封鎖等候一個資料流程，因為它會嘗試交錯兩個數據流。 在執行圖形之前，請在所有的捕獲資料流程上設定相同的開始和停止時間：


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



就內部而言， **ControlStream** 方法會使用 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面，此介面會在捕捉篩選器的釘選上、Smart t 濾波器 (（如果有的話) ，也可能是 mux 篩選器）。 您可以直接使用此介面，而不是呼叫 **ControlStream**，不過這樣做並沒有任何特定的優點。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



