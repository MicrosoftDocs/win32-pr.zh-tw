---
title: '在 DirectShow 中讀取 ASF 檔案 (Windows Media Format 11 SDK) '
description: 在 DirectShow 中讀取 ASF 檔案
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，讀取 ASF 檔案
- Windows Media Format SDK，WM ASF 讀取器篩選器
- Windows Media Format SDK，IMediaSeeking 介面
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
- Advanced Systems Format (ASF) 、WM ASF 讀取器篩選器
- ASF (Advanced Systems Format) 、WM ASF Reader 篩選器
- Advanced Systems Format (ASF) ，IMediaSeeking 介面
- ASF (Advanced Systems Format) ，IMediaSeeking 介面
- DirectShow，讀取 ASF 檔案
- DirectShow、WM ASF 讀取器篩選器
- DirectShow、IMediaSeeking 介面
- WM ASF 讀取器篩選器
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf7ba34444f4a3b46f4413958bd26ba4bafc8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317035"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>在 DirectShow 中讀取 ASF 檔案 (Windows Media Format 11 SDK) 

ASF 檔案的播放是由 [WM Asf 讀取](wm-asf-reader-filter.md) 器篩選器所處理。 當 WM ASF 讀取器讀取檔案時，它會自動建立每個資料流程的輸出針腳，包括 Web 資料流程、指令碼命令資料流程，以及任何其他類型的任意資料流程。 如果是多位元率檔案，則只會針對目前選取的資料流程建立 pin。

WM ASF 讀取器支援 DirectShow **IMediaSeeking** 介面，可讓應用程式在檔案內執行時態搜尋。 但是，不支援以 **IMediaSeeking：： SetRate**) 中所指定的 1.0 (速度來播放。

篩選準則也會公開數個 Windows Media 格式 SDK 介面，如下表所述。



| 介面                                        | 公開的方式                            | 註解                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | 透過篩選器上的 **IServiceProvider** | 適用于需要播放由數位 Rights Management (DRM) 所保護之內容的應用程式。 這個介面也可以用來直接取得讀取器物件上的其他介面。 |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | 篩選上的 **QueryInterface**           | 提供讓應用程式可以讀取檔案和內容屬性，以及標記和腳本資訊和中繼資料。                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | 篩選上的 **QueryInterface**           | 部分實作為篩選準則，讓應用程式可以存取 WM 讀取器物件上的資訊方法。                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | 篩選上的 **QueryInterface**           | 部分實作為篩選器，讓應用程式可以存取 Reader 物件上的參考方法。                                                                         |



 

已先將 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器提供給 DirectShow 8.0。 DirectShow 8.1 和9.0 隨附的篩選版本支援第7版。Windows Media 格式 SDK *x* 。 最新版本的篩選器和其他 QASF 元件會隨附于並支援 Windows Media Format 9 系列 SDK 和更新版本，並取代 DirectX 9.0 中的篩選器。 如果您在安裝 DirectX 8 之後安裝 Windows Media Format SDK。*x* 或9。*x* SDK，您將會以9系列版本覆寫 qasf.dll 的 DirectX 版本。 這應該不會顯示任何問題，但可能在某個情況下，可能會導致 DirectShow **IGraphBuilder：： RenderFile** 方法中有不同的行為。 WM ASF 讀取器的 Windows Media Format 9 系列 SDK 版本是 .asf、.wmv 和 .wma 副檔名的預設來源篩選器。 這表示當指定了這個類型的檔案時，會自動建立 WM ASF 讀取器，並將其加入至篩選圖形中的方法（例如 **IGraphBuilder：： RenderFile** 或 **IGraphBuilder：： AddSourceFilter** ）。 在 DirectX 9.0 及更早版本，以及 Windows XP Service Pack 1 及更早版本中， **RenderFile** 方法會使用較舊的 Windows Media 來源篩選。 維護此行為的目的，是為了確保與使用 Windows Media Player 6.4 的應用程式回溯相容。 如需舊版 Windows Media 來源篩選器的詳細資訊，請參閱 DirectShow SDK 檔。

若要使用 WM ASF 讀取器以 Windows Media 內容播放 ASF 檔案，三個主要步驟是建立篩選圖形管理員的實例，呼叫 **IGraphBuilder：： RenderFile** 來建立圖形，然後呼叫 **IMediaControl：： Run** 來播放該檔案。 下列程式碼範例是使用 DirectShow 播放 ASF 檔案的完整程式。 若要執行此範例，您必須安裝 DirectX SDK，而且必須根據 DirectShow SDK 檔主題「設定組建環境」中的指示來設定您的組建環境。 此外，您必須在您的電腦上，于 **RenderFile** 的呼叫中指定檔案。


```C++
#include <dshow.h>
#include <stdio.h>

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

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
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



請注意，這個簡單範例的應用程式程式碼絕對不會明確參考 WM ASF 讀取器。 篩選圖形管理員會建立、連線、執行和最後發行該篩選。 不過，在許多情況下，您可能會想要先設定 WM ASF 讀取器，再開始播放。

 

 




