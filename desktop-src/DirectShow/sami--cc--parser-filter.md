---
description: " (CC) 剖析器篩選器的薩米文"
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: " (CC) 剖析器篩選器的薩米文"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0449bccd41a09fca952b5d84552ef919055526
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510171"
---
# <a name="sami-cc-parser-filter"></a> (CC) 剖析器篩選器的薩米文

剖析從已同步處理的可存取媒體交換的資料字幕資料 (薩米) 的檔案。

薩米文是類似于 HTML 的文字格式，用於編碼以時間為基礎的標題。 此篩選會將薩米的資料轉換成文字資料流程。 資料流程中的每個範例都包含一個標題專案，以及格式資訊。 範例上的時間戳記是從薩米文檔案中的時間資訊產生的。

此篩選器的設計目的是要搭配 [內部指令碼命令](internal-script-command-renderer-filter.md) 轉譯器篩選準則使用。 內部指令碼命令轉譯器會接收文字範例，並以事件通知的形式將它們傳送至應用程式。 如需詳細資訊，請參閱＜備註＞一節。



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)、 [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| 輸入 Pin 媒體類型                    | 媒體媒體的 \_ 串流                                                                                        |
| 輸入 Pin 介面                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| 輸出 Pin 媒體類型                   | 媒體 \_ 文字、MEDIASUBTYPE \_ Null                                                                      |
| 輸出 Pin 介面                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                         |
| 可執行檔                               | quartz.dll                                                                                               |
| [優點](merit.md)                       | 不 \_ 太可能                                                                                          |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>備註

以下是一個簡單的薩米文檔案：


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



**STYLE** 標記會定義兩種語言設定：英文 (。ENCC) 和法文 (。FRCC) 。 它也會定義兩種樣式： \# 標準和 \# GREENTEXT。 每個 **同步** 標記會定義標題的開始時間（以毫秒為單位）。 **P** 標記包含標題文字，而 **類別** 屬性則會指定要套用標題的語言設定。

針對每個語言和樣式，此篩選準則會建立邏輯資料流程。 在任何時候，都只會啟用一個語言資料流程和一個樣式資料流程。 當篩選準則產生範例時，它會選取目前語言的標題，並套用目前的樣式。 預設會啟用在檔案中宣告的第一個語言和樣式。 應用程式可以使用 [**IAMStreamSelect：： enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) 方法來啟用不同的資料流程。

使用預設設定時，範例檔案中的第一個標題會產生下列輸出：


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



如果輸出移至內部指令碼命令轉譯器，則該篩選準則會傳送 [**EC \_ OLE \_ 事件**](ec-ole-event.md) 事件通知。 第二個事件參數是具有標題文字的 BSTR。 應用程式可以取出事件並顯示標題。

下列範例顯示如何轉譯薩米文的檔案、取出串流資訊、啟用資料流程，以及顯示標題文字。 此範例假設先前的薩米文檔案儲存為 C： \\ 薩米文的 \_ 測試檔案 \_ 。

為了簡潔起見，此範例會在呼叫 **IAMStreamSelect：： Enable** 方法時使用硬式編碼的資料流程索引。 它也會執行基本的錯誤檢查。


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



此篩選器會使用 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面從來源篩選器提取範例。 因此，它不支援其輸入 pin 上的 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



