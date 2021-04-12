---
description: 如何播放檔案
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: 如何播放檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385803"
---
# <a name="how-to-play-a-file"></a>如何播放檔案

本文旨在提供您 DirectShow 程式設計的特色。 它會顯示一個簡單的主控台應用程式，可播放音訊或影片檔案。 程式只有幾行時間，但它會示範一些 DirectShow 程式設計的威力。

在「 [Directshow 應用程式程式設計」簡介](introduction-to-directshow-application-programming.md) 文章中，directshow 應用程式一律會執行相同的基本步驟：

1.  建立 [篩選圖形管理員](filter-graph-manager.md)的實例。
2.  使用篩選圖形管理員來建立篩選圖形。
3.  執行圖形，使資料在篩選準則下移動。

若要編譯及連結此主題中的程式碼，請包含標頭檔 Dshow，並連結至靜態程式庫檔案 strmiids。 如需詳細資訊，請參閱 [建立 DirectShow 應用程式](setting-up-the-build-environment.md)。

首先，呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 初始化 COM 程式庫：


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



為了簡單起見，此範例會忽略傳回值，但您應該一律從任何方法呼叫中檢查 **HRESULT** 值。

接下來，呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立篩選圖形管理員：


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



如所示， (CLSID) 的類別識別碼是 CLSID \_ FilterGraph。 篩選圖形管理員是由同進程 DLL 提供，因此執行內容是 **CLSCTX \_ INPROC \_ SERVER**。 DirectShow 支援自由執行緒模型，因此您也可以使用 **COINIT \_ 多執行緒** 旗標來呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 。

對 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 的呼叫會傳回 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面，此介面大多包含用來建立篩選圖形的方法。 此範例需要兩個其他介面：

-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 控制項串流處理。 它包含用來停止和啟動圖形的方法。
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 具有從篩選圖形管理員取得事件的方法。 在此範例中，會使用介面來等候播放完成。

這兩個介面都是由篩選圖形管理員所公開。 使用傳回的 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 指標來查詢它們：


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



現在您可以建立篩選圖形。 針對檔案播放，這是透過單一方法呼叫來完成：


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



[**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)方法會建立可播放指定檔案的篩選圖形。 第一個參數是檔案名，以寬字元表示 (2 位元組) 字串。 第二個參數是保留的，而且必須等於 **Null**。

如果指定的檔案不存在，或無法辨識檔案格式，這個方法可能會失敗。 不過，假設此方法成功，則篩選圖形現在已準備好進行播放。 若要執行圖形，請呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 方法：


```C++
hr = pControl->Run();
```



當篩選圖形執行時，資料會在篩選器中移動，並轉譯成影片和音訊。 播放會在個別的執行緒上執行。 您可以藉由呼叫 [**IMediaEvent：： WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) 方法來等候播放完成：


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



這個方法會封鎖直到檔案完成播放為止，或直到指定的逾時間隔到期為止。 值無限大表示應用程式會無限期地封鎖，直到檔案完成播放為止。 如需事件處理的更實際範例，請參閱 [回應事件](responding-to-events.md)。

當應用程式完成時，請釋放介面指標並關閉 COM 程式庫：


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>範例程式碼

以下是本文所述範例的完整程式碼：


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本的 DirectShow 工作](basic-directshow-tasks.md)
</dt> </dl>

 

 
