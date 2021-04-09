---
description: 建立 VMR 9 篩選圖形
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: 建立 VMR 9 篩選圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846567"
---
# <a name="building-a-vmr-9-filter-graph"></a>建立 VMR 9 篩選圖形

由於影片混合轉譯器9篩選 (VMR-9) 不是預設的影片轉譯器，因此使用 VMR-9 的應用程式必須明確地將它新增至圖形並進行連接。 本節提供兩種不同的方法，可使用 VMR-9 建立篩選圖形。

使用 Capture Graph Builder

「捕獲圖形產生器」是用來建立自訂篩選圖形的協助程式物件。 您可以使用它來建立 VMR 9 圖形，如下所示：

1.  建立並初始化「Capture Graph 建立器」，如「 [捕獲圖形](about-the-capture-graph-builder.md)產生器」主題所述。
2.  呼叫 CoCreateInstance 以建立 VMR-9：
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  在篩選圖形管理員上呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) ，將 VMR-9 新增至篩選圖形：
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  呼叫 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) 以新增影片檔案的來源篩選：
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，以將影片資料流程轉譯為 VMR：
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  （選擇性）再次呼叫 RenderStream，以轉譯音訊串流：
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

您可以針對每個原始程式檔呼叫 AddSourceFilter 和 RenderStream，以混合數個影片串流。

使用篩選圖形管理員

如果您不想使用 [Capture Graph Builder]，可以使用 [篩選圖形管理員] 上的方法來建立 VMR 9 圖形，如下所示：

1.  建立 VMR-9 並將它新增至圖形，如先前的程式所示。
2.  使用 AddSourceFilter 來新增影片檔案的來源篩選器，如先前的程式所示。
3.  如果您想要轉譯音訊，請建立 [DirectSound](directsound-renderer-filter.md) 轉譯器篩選器的實例，並將它加入至篩選圖形。
4.  使用 IBaseFilter：： EnumPins 方法來尋找來源篩選器上的輸出圖釘。 如需詳細資料，請參閱 [列舉釘](enumerating-pins.md) 選。
5.  查詢 IFilterGraph2 介面的篩選圖形管理員。
6.  使用 AM RenderEx RENDERTOEXISTINGRENDERERS 旗標呼叫 [**IFilterGraph2：： RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) \_ \_ 。 此呼叫只會使用已在圖形中的轉譯器篩選器（在此案例中為 VMR-9 和 DirectSound 轉譯器）來呈現輸出圖釘。 這可防止智慧型 Connect 邏輯將預設影片轉譯器新增至圖形，這會讓 VMR-9 保持未連接。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Capture Graph Builder 建立圖形](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



