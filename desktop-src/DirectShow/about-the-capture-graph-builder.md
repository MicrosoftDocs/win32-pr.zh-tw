---
description: 關於 Capture Graph Builder
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: 關於 Capture Graph Builder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ef82a160ada6e53fe6d2db830efa85118eb699074630905cd41f0b5412ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664511"
---
# <a name="about-the-capture-graph-builder"></a>關於 Capture Graph Builder

執行影片或音訊捕獲的篩選圖形稱為「 *捕獲圖形*」。 捕捉圖形通常比檔案播放圖形更為複雜。 為了讓應用程式能更輕鬆地建立組建圖形，DirectShow 提供一個 helper 物件，稱為 capture Graph Builder。 capture Graph Builder 會公開 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)介面，其中包含用來建立和控制捕捉圖形的方法。 下圖說明 Capture Graph Builder 和 **ICaptureGraphBuilder2** 介面。

![使用 capture graph builder](images/cgb01.png)

首先，呼叫 CoCreateInstance 來建立 Capture Graph 產生器的新實例和篩選 Graph 管理員。 然後藉由呼叫 [**ICaptureGraphBuilder2：： SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph)與篩選 Graph 管理員 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)介面的指標，初始化 Capture Graph Builder。 下圖說明此程序。

![初始化 capture graph builder](images/cgb03.png)

下列程式碼顯示 helper 函式來執行這些步驟：


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



在這一節的影片捕獲中，假設您使用 capture Graph Builder 建立 capture Graph。 不過，您可以使用 IGraphBuilder 方法，完全建立 capture 圖形。 不過，這是一個很好的主題，而且偏好使用 Capture Graph Builder 方法。 如需詳細資訊，請參閱「 [Advanced Capture」主題](advanced-capture-topics.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DirectShow 中的影片捕獲](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



