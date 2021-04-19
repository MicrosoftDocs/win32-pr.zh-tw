---
description: 記憶體壓力報告可讓 Direct3D 應用程式判斷其影片記憶體工作集是否成長過大。
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: 記憶體壓力報告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996651"
---
# <a name="memory-pressure-reporting"></a>記憶體壓力報告

記憶體壓力報告可讓 Direct3D 應用程式判斷其影片記憶體工作集是否成長過大。

*記憶體壓力* 是應用程式放在記憶體子系統上的需求。 雖然任何 Direct3D 應用程式都可以使用記憶體壓力報告，但這項功能特別適用于使用 Direct3D 呈現影片的應用程式。 影片播放通常受益于大量的緩衝，因此可以事先解碼框架。 雖然緩衝處理通常會使播放更順暢，但如果工作集成長太大，則可能會因為下列因素而導致效能降低：

-   記憶體可能會從快取中收回。 在最糟的情況下，這可能會發生在每個影片畫面上。
-   記憶體配置可能會放置在非最佳的記憶體區段中。

從 Windows 7 開始，Direct3D 可以報告關於影片記憶體壓力的一些統計資料：

-   進程在一段時間內收回的位元組數目。
-   放在非最非最佳記憶體區段中的記憶體數量。
-   粗略指出記憶體配置放在非最佳記憶體的整體效率。

此資訊可協助應用程式維護合理的工作集。

## <a name="using-memory-pressure-reporting"></a>使用記憶體壓力報告

記憶體壓力報告使用現有的 **IDirect3DQuery9** 介面來查詢裝置。 已將新的查詢類型加入至 **D3DQUERYTYPE** 列舉。


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



若要使用此查詢，請執行下列步驟：

1.  使用 **D3DQUERYTYPE \_ MEMORYPRESSURE** 旗標呼叫 **IDirect3DDevice9Ex：： CreateQuery** 。 這個方法會傳回 **IDirect3DQuery9** 介面的指標。
2.  使用 **D3DISSUE \_ 開始** 旗標呼叫 **IDirect3DQuery9：： Issue** 開始度量間隔。
3.  使用 **D3DISSUE \_ 結束** 旗標呼叫 **IDirect3DQuery9：： Issue** 。
4.  呼叫 **IDirect3DQuery9：：** 以取得查詢結果。 此查詢會傳回 [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) 結構。

## <a name="example-code"></a>範例程式碼

下列範例顯示兩個測量記憶體壓力的函數。 第一個會開始測量間隔，而第二個則會抓取測量結果。


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 影片 Api](direct3d-video-apis.md)
</dt> </dl>

 

 



