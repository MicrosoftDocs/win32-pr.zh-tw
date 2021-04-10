---
description: 使用 Capture Graph Builder 建立圖形
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: 使用 Capture Graph Builder 建立圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846728"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a>使用 Capture Graph Builder 建立圖形

不論其名稱，Capture Graph Builder 都可用於建立許多種類的自訂篩選圖形，而不只是捕捉圖形。 本文提供如何使用此物件的簡短總覽。

[Capture Graph Builder] 會公開 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面。 首先，呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立「捕獲圖形產生器」和「篩選圖形管理員」。 然後藉由呼叫 [**ICaptureGraphBuilder2：： SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) 與篩選圖形管理員的指標，初始化 Capture Graph Builder，如下所示：


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a>連接篩選

[**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法會將兩個或三個篩選器一起連接在一個鏈中。 一般來說，當每個篩選準則的輸入 pin 或輸出 pin 類型相同時，方法的效果最好。 這項討論一開始會忽略 **RenderStream** 的前兩個參數，並將焦點放在最後三個參數。 第三個參數是 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 指標，可將篩選 (指定為 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面指標) 或輸出釘選 (做為 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標) 。 第四個和第五個參數指定 **IBaseFilter** 指標。 **RenderStream** 方法會連接鏈中的所有三個篩選準則。 例如，假設 *A*、 *B* 和 *C* 是篩選準則。 假設現在每個篩選都只有一個輸入 pin 和一個輸出圖釘。 下列呼叫會將 A 連接到 B，然後從 B 到 C：

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

所有連線都是「智慧型」的，也就是說，其他篩選器會視需要新增至圖形。 如需詳細資訊，請參閱 [智慧型 Connect](intelligent-connect.md)。 若只連接兩個篩選器，請將中間值設定為 **Null**。 例如，這個呼叫會將 A 連接到 C：

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

您可以呼叫方法兩次，以建立較長的鏈：

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

如果最後一個參數為 **Null**，則方法會自動尋找預設轉譯器。 它會使用影片的 [影片](video-renderer-filter.md) 轉譯器，以及適用于音訊的 [DirectSound](directsound-renderer-filter.md) 轉譯器。 因此：

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

相當於

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

其中 *R* 是適當的轉譯器。 不過，若要連接視頻混合轉譯器篩選器，而不是影片轉譯器，您必須明確指定。

如果您在第三個參數中指定篩選，而不是使用 pin 碼，您可能需要指定連接所應使用的輸出圖釘。 這是方法前兩個參數的用途。 第一個參數只適用于 capture 篩選。 它會指定指出釘選類別的 GUID。 如需完整的類別清單，請參閱 [釘選屬性集](pin-property-set.md)。 以下兩個類別對所有的捕獲篩選都有效：

-   **釘選 \_ 類別 \_ 捕獲**
-   **釘選 \_ 類別 \_ 預覽**

如果捕捉篩選未提供個別的 pin 供捕捉和預覽，則 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法會插入 [智慧型的 t](smart-tee-filter.md) a 濾波器，將資料流程分割成捕獲資料流程和預覽資料流程。 從應用程式的觀點來看，您可以直接將所有的捕獲篩選器視為具有個別的 pin，並忽略圖形的基礎拓撲。

針對 [檔案捕獲]，將捕捉 pin 連接至 mux 篩選器。 若為即時預覽，請將預覽釘選到轉譯器。 如果您切換兩個類別，則圖形可能會在檔案捕獲期間卸載過多的畫面格數目;但是，如果圖表已正確連接，它會視需要卸載預覽畫面格，以維持捕獲資料流程的輸送量。

下列範例顯示如何連接兩個數據流：


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



某些 capture 濾波器也支援隱藏式輔助字幕，以 **釘選 \_ 類別 \_ VBI** 表示。 若要將隱藏式輔助字幕捕捉至檔案，請將此類別轉譯為 mux 篩選器。 若要在預覽視窗中查看隱藏式輔助字幕，請連接到轉譯器：


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



[**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)的第二個參數會識別媒體類型，而且通常是下列其中一項：

-   媒體 \_ 媒體
-   媒體 \_ 媒體
-   以 \_) 交錯 (DV 的媒體

只要篩選的輸出圖釘支援慣用媒體類型的列舉，您就可以使用這個參數。 針對檔案來源，[Capture Graph Builder] 會視需要自動新增剖析器篩選，然後查詢剖析器上的媒體類型。  (如需範例，請參閱 [RECOMPRESSING AVI](recompressing-an-avi-file.md)檔。 ) 此外，如果鏈中的最後一個篩選器有數個輸入圖釘，方法會嘗試列舉其媒體類型。 不過，並非所有篩選都支援此功能。

## <a name="finding-interfaces-on-filters-and-pins"></a>尋找篩選和釘選介面

建立圖形之後，您通常需要找出圖形中的篩選和釘選所公開的各種介面。 例如，「捕捉」篩選器可能會公開 [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) 介面，而篩選的輸出圖釘可能會公開 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面。

尋找介面最簡單的方式是使用 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法。 這個方法會將圖形 (篩選和釘選) ，直到它找到所需的介面為止。 您可以指定搜尋的起點，也可以限制搜尋從起始點篩選上游或下游。

下列範例會在影片預覽釘選上搜尋 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面：


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> 主題 [尋找篩選或釘選上的介面](find-an-interface-on-a-filter-or-pin.md) 時，會顯示使用 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面而非 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)的替代方法。 使用哪一種方法取決於您的應用程式。 如果您的應用程式已經使用 **ICaptureGraphBuilder2** 來建立圖形，則 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 是不錯的方法。 否則，請考慮使用 **IGraphBuilder** 方法。

 

## <a name="finding-pins"></a>尋找釘選

一般來說，您可能需要在篩選器上找出個別的 pin，不過在大部分情況下， [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 和 [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法會為您節省問題。 如果您需要在篩選準則中尋找特定的 pin， [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper 方法會很有用。 指定類別、媒體類型 (影片或音訊) 、方向，以及 pin 是否必須連接。

例如，下列程式碼會在捕獲篩選器上搜尋未連接的影片預覽 pin：


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 
