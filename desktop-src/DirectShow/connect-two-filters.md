---
description: 本主題說明用來連接 DirectShow 篩選器的一些協助程式函式。
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: 連接兩個篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109413"
---
# <a name="connect-two-filters"></a>連接兩個篩選器

本主題說明用來連接 DirectShow 篩選器的一些協助程式函式。

若要連接兩個篩選器，您必須在上游篩選器上找到未連接的輸出 pin，以及下游篩選器上未連接的輸入 pin。

如果您已經有兩個釘選的指標，請呼叫 [**IGraphBuilder：： connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) 方法來連接它們。 如果 pin 無法直接連接到彼此， **IGraphBuilder：： connect** 方法可能會插入其他篩選器，以完成連線。 如需詳細資訊，請參閱 [智慧型 Connect](intelligent-connect.md)。

如果您有指向篩選準則的指標，而不是釘選，您必須使用 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 方法來尋找釘選。  (參閱 [列舉釘](enumerating-pins.md)選。 ) 本主題中的 helper 函式會示範這項技巧。

### <a name="output-pin-to-filter"></a>輸出釘選至篩選

下列函式會採用兩個參數：輸出圖釘的指標，以及篩選的指標。 此函式會將輸出圖釘連接至篩選上的第一個可用輸入圖釘。


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



此函式會執行下列工作：

1.  呼叫函 `FindUnconnectedPin` 式以取得未連接的輸入 pin。 此函式會顯示在 [篩選器的 [尋找未](find-an-unconnected-pin-on-a-filter.md)連接的 Pin] 主題中。
2.  呼叫 [**IGraphBuilder：： connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) 來連接兩個圖釘。

### <a name="filter-to-input-pin"></a>篩選至輸入釘選

下一個函式會接受篩選的指標和指向輸入圖釘的指標。 它會將輸入釘選到篩選器上的第一個可用輸出圖釘。


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a>篩選篩選

第三個函式會接受上游篩選的指標和下游篩選的指標，並嘗試連接這兩個篩選準則。


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般 Graph-Building 技術](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



