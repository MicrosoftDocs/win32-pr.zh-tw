---
description: 將專案寫入檔案
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: 將專案寫入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980325"
---
# <a name="writing-a-project-to-a-file"></a>將專案寫入檔案

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本文說明如何將 [DirectShow 編輯服務](directshow-editing-services.md) 專案寫入檔案。 首先，它會說明如何使用基本轉譯引擎來寫入檔案。 然後，它會使用智慧型轉譯引擎來描述智慧型 recompression。

如需有關「DirectShow 編輯服務」如何轉譯專案的總覽，請參閱 [關於呈現引擎](about-the-render-engines.md)。

**使用基本轉譯引擎**

首先，建立圖形的前端，如下所示：

1.  建立轉譯引擎。
2.  指定時間軸。
3.  設定呈現範圍。 (選用)
4.  建立圖形的前端。

下列程式碼範例顯示這些步驟。


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



接下來，將多工器和檔案寫入篩選器新增至篩選圖形。 若要這麼做，最簡單的方式就是使用「 [捕獲圖形](capture-graph-builder.md)產生器」，這是用來建立捕獲圖形的 DirectShow 元件。 [Capture graph builder] 會公開 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面。 執行下列步驟：

1.  建立「capture graph 建立器」的實例。
2.  取得圖形的指標，並將其傳遞至 graph builder。
3.  指定輸出檔案的名稱和媒體類型。 此步驟也會取得 mux 篩選的指標，稍後需要此篩選器。

下列程式碼範例顯示這些步驟。


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



最後，將前端的輸出圖釘連接至 mux 篩選器。

1.  取出群組的數目。
2.  針對每個 pin，取得釘選的指標。
3.  （選擇性）建立壓縮篩選準則的實例，以壓縮資料流程。 [壓縮程式] 的類型會視群組的媒體類型而定。 您可以使用 [系統裝置](system-device-enumerator.md) 列舉值來列舉可用的壓縮篩選。 如需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。
4.  （選擇性）設定壓縮參數，例如金鑰畫面播放速率。 本文稍後會詳細討論此步驟。
5.  呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)。 這個方法會取得釘選的指標，壓縮篩選器 (是否有任何) 和多工器。

下列程式碼範例示範如何連接輸出圖釘。


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



若要設定壓縮參數 (步驟4（先前) ），請使用 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面。 此介面會公開于壓縮篩選的輸出圖釘上。 列舉壓縮篩選器的釘選，然後查詢每個輸出的 pin 以進行 **IAMVideoCompression**。  (如需列舉釘選的詳細資訊，請參閱 [列舉釘](enumerating-pins.md)選。 ) 務必釋出您在此步驟中取得的所有介面指標。

在您建立篩選圖形之後，請在篩選圖形管理員上呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 方法。 當篩選圖形執行時，它會將資料寫入檔案。 使用事件通知來等候播放完成。  (查看 [回應事件](responding-to-events.md)) 。播放完成時，您必須明確呼叫 [**IMediaControl：： stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) 以停止篩選圖形。 否則，就不會正確寫入檔案。

**使用智慧型轉譯引擎**

若要取得智慧 recompression 的優點，請使用智慧型轉譯引擎取代基本轉譯引擎。 建立圖形的步驟幾乎相同。 主要差異在於，壓縮是在圖形的前端處理，而不是在檔案寫入區段中處理。

> [!IMPORTANT]
> 請勿使用智慧型轉譯引擎來讀取或寫入 Windows Media 檔案。

 

每個影片群組都有一個屬性，可指定該群組的壓縮格式。 壓縮格式必須完全符合群組的高度、寬度、位深度和畫面播放速率的未壓縮格式。 智慧型轉譯引擎會使用壓縮格式來建立圖形。 設定壓縮格式之前，請務必藉由呼叫 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md)，為該群組設定未壓縮的格式。

若要設定群組的壓縮格式，請呼叫 [**IAMTimelineGroup：： SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) 方法。 這個方法會採用 [**SCompFmt0**](scompfmt0.md) 結構的指標。 **SCompFmt0** 結構有兩個成員： **nFormatId**，其必須為零 **，而**[**媒體類型為 AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構。 使用格式資訊來初始化 **AM \_ 媒體 \_ 類型** 結構。

> [!Note]  
> 如果您想要讓最終專案具有與其中一個原始程式檔相同的格式，您可以 \_ 使用媒體偵測器 \_ ，直接從原始程式檔取得 AM 媒體類型結構。 請參閱 [**IMediaDet：： get \_ StreamMediaType**](imediadet-get-streammediatype.md)。

 

將 [**SCompFmt0**](scompfmt0.md) 變數轉換為 **long** 類型的指標，如下列範例所示。


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



智慧型轉譯引擎會自動搜尋相容的壓縮篩選。 您也可以藉由呼叫 [**ISmartRenderEngine：： SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md)來指定群組的壓縮篩選。

若要建立圖形，請使用上一節中針對基本轉譯引擎所述的相同步驟。 唯一的差異如下：

-   使用智慧型轉譯引擎，而不是基本轉譯引擎。 類別識別碼是 CLSID \_ SmartRenderEngine。
-   在您建立前端之後，但在呈現輸出圖釘之前，請設定壓縮參數。 呼叫 [**ISmartRenderEngine：： GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) 方法，以取得群組壓縮篩選的指標。 然後查詢 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面，如先前所述。
-   當您呈現輸出圖釘時，不需要插入壓縮篩選。 資料流程已壓縮。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯專案](rendering-a-project.md)
</dt> </dl>

 

 



