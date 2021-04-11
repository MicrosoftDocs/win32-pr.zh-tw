---
description: 建立 Recompression 圖形
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: 建立 Recompression 圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845855"
---
# <a name="building-the-recompression-graph"></a>建立 Recompression 圖形

AVI 檔案 recompression 的一般篩選圖形看起來如下所示：

![avi recompression 圖形](images/avi2avi4.png)

[AVI 分隔器篩選器](avi-splitter-filter.md)會從檔案[來源提取資料 (Async) 篩選器](file-source--async--filter.md)，並將它剖析成影片和音訊串流。 影片解壓縮程式會將壓縮的影片解碼，而影片壓縮程式會 recompressed 此影片。 Decompressors 的選擇取決於原始程式檔;它會由 [智慧型 Connect](intelligent-connect.md)自動處理。 應用程式必須選擇壓縮程式，通常是向使用者呈現清單。  (，請參閱 [選擇壓縮篩選](choosing-a-compression-filter.md)。 ) 

壓縮的影片接著會進入 [AVI Mux 篩選器](avi-mux-filter.md)。 此範例中的音訊串流未壓縮，因此會直接從 AVI 分隔器移至 AVI Mux。 AVI Mux 會交錯兩個數據流，而檔案 [寫入器篩選器](file-writer-filter.md) 會將輸出寫入磁片。 請注意，即使原始檔案沒有音訊資料流程，也需要 AVI Mux。

建立此篩選圖形最簡單的方式是使用「 [捕獲圖形](capture-graph-builder.md)產生器」，這是用來建立捕獲圖形和其他自訂篩選圖形的 DirectShow 元件。

首先，呼叫 CoCreateInstance 以建立「捕獲圖形產生器」：


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



然後使用 [Capture Graph Builder] 來建立篩選圖形：

1.  建立圖形的轉譯區段，其中包括 AVI Mux 篩選器和檔案 [寫入](file-writer-filter.md)器。
2.  將來源篩選和壓縮篩選新增至圖形。
3.  將來源篩選連接至 MUX 篩選器。 「捕獲圖形產生器」會插入剖析來源檔案時所需的任何分隔器和解碼篩選器。 它也可以透過壓縮篩選器來路由傳送影片和音訊串流。

下列各節將說明每個步驟。

建立轉譯區段

若要建立圖形的轉譯區段，請呼叫 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) 方法。 這個方法會採用輸入參數，以指定輸出的媒體子類型和輸出檔的名稱。 它會傳回 MUX 篩選器和檔案寫入器的指標。 下一階段的 graph 大樓需要 MUX 篩選器。 這個範例不需要檔案寫入器的指標，所以參數可以是 **Null**：


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



當方法傳回時，MUX 篩選具有未處理的參考計數，因此請務必稍後再釋放指標。

下圖顯示此時間點的篩選圖形。

![篩選圖形的轉譯區段](images/avi2avi1.png)

MUX 篩選器會公開兩個介面來控制 AVI 格式：

-   [**IConfigInterleaving 介面**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)：設定交錯模式。
-   [**IConfigAviMux 介面**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)：設定主要資料流程和 AVI 相容性索引。

新增來源和壓縮篩選

下一步是要將來源和壓縮篩選新增至篩選圖形。 當您呼叫 SetOutputFileName 時，「捕獲圖形產生器」會自動建立篩選圖形管理員的實例。 藉由呼叫 [**ICaptureGraphBuilder2：： GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) 方法取得其指標：


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



現在呼叫 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) 方法以新增非同步檔案來源篩選，並呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法以新增影片壓縮程式：


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



此時，來源篩選和壓縮篩選不會連接到圖形中的任何其他內容，如下圖所示：

![具有來源和壓縮篩選的篩選圖形](images/avi2avi2.png)

將來源連線至 Mux

最後一個步驟是透過影片壓縮程式，將來源篩選器連線到 AVI Mux 篩選器。 使用 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，將來源篩選上的輸出連接連接到指定的接收篩選（選擇性地透過壓縮篩選）。

前兩個參數指定釘選類別和媒體類型，以指定要連接的來源篩選器 pin。 非同步檔案來源篩選只有一個輸出圖釘，因此這些參數應為 **Null**。 接下來的三個參數會指定來源篩選準則、壓縮篩選 (是否有任何) 和 Mux 篩選器。

下列程式碼範例會透過影片壓縮程式呈現影片串流：


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



下圖顯示到目前為止的篩選圖形。

![轉譯的影片資料流程](images/avi2avi3.png)

假設原始程式檔有音訊串流， [AVI 分隔](avi-splitter-filter.md) 器篩選器已建立音訊的輸出圖釘。 若要連接此 pin，請再次呼叫 RenderStream：


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



此處未指定壓縮篩選。 來源篩選的輸出釘選已連線，因此 RenderStream 方法會在分隔器篩選器上搜尋未連接的輸出 pin。 它會尋找音訊 pin 碼，並將它直接連接到 MUX 篩選器。 如果來源檔案沒有音訊串流，則第二次呼叫 RenderStream 將會失敗。 這是正常的現象。 圖形是在第一次呼叫 RenderStream 之後完成，因此第二次呼叫中的失敗是無害的。

在此範例中，兩個 RenderStream 呼叫的順序很重要。 因為第二個呼叫不會指定壓縮器，所以會從 AVI 分隔器連接任何未連接的 pin。 如果您在另一個呼叫之前進行此呼叫，它可能會將影片資料流程連接到 AVI Mux，而不需要您的影片壓縮程式。 因此， (具有壓縮篩選) 的特定呼叫必須先發生。

先前的討論假設原始程式檔是 AVI 檔。 不過，這項技術也適用于其他檔案類型，例如 MPEG 檔。 產生的篩選圖形會稍有不同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Recompressing AVI 檔案](recompressing-an-avi-file.md)
</dt> </dl>

 

 



