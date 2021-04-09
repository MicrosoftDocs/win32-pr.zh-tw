---
description: 本主題描述自訂的 DirectShow capture 篩選器應該如何產生輸出資料。
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: 在 Capture 篩選器中產生資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935877"
---
# <a name="producing-data-in-a-capture-filter"></a>在 Capture 篩選器中產生資料

本主題描述自訂的 DirectShow capture 篩選器應該如何產生輸出資料。

## <a name="filter-state-changes"></a>篩選狀態變更

只有在執行篩選時，才會產生資料的捕獲篩選。 當篩選暫停時，請勿從您的 pin 傳送資料。 此外，當篩選暫停時，傳回 VFW 無法從 [**CBaseFilter：： >getstate**](cbasefilter-getstate.md)方法 **\_ \_ \_ 提示**。 此傳回值會告知篩選圖形管理員，在篩選暫停時，不應該等候篩選中的任何資料。 如需詳細資訊，請參閱 [篩選狀態](filter-states.md)。

下列程式碼顯示如何執行 [**IMediaFilter：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) 方法：


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a>控制個別資料流程

捕捉篩選器的輸出圖釘應支援 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面，讓應用程式可以個別開啟或關閉每個 pin。 例如，應用程式可以在不進行捕捉的情況下預覽，然後切換到 [capture] 模式，而不需重建篩選圖形。 您可以使用 [**CBaseStreamControl**](cbasestreamcontrol.md) 類別來執行這個介面。

## <a name="time-stamps"></a>時間戳記

當篩選器捕捉到範例時，請使用目前的資料流程時間來為範例加上時間戳記。 結束時間是開始時間加上持續時間。 例如，如果篩選器是以每秒10個樣本來進行，而且當篩選器捕捉到樣本時，資料流程時間為200000000個單位，則時間戳記應該是200000000和201000000。  (每秒10000000個單位。 ) 

若要計算資料流程時間，請呼叫 [**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 方法來取得目前的參考時間，然後減法原始的開始時間。 或者，呼叫 [**CBaseFilter：： StreamTime**](cbasefilter-streamtime.md) 方法，它會執行相同的計算。 若要設定範例的時間戳記，請呼叫 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 方法。

不過，如果篩選具有預覽 pin，則來自預覽 pin 的範例不應該有時間戳記。 原因是，在捕捉時間之後，範例一律會稍微觸及轉譯器。 如果樣本有時間戳記，轉譯器會將它們視為延遲，而且可能會藉由卸載樣本來嘗試趕上。  (需詳細資訊，請參閱 [DirectShow 影片捕獲篩選器](directshow-video-capture-filters.md)。 ) 請注意， [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面需要 pin 才能追蹤取樣時間。 針對預覽釘選，您可能需要修改執行，使其不依賴時間戳記。

時間戳記必須永遠從一個樣本增加到下一個樣本。 即使在篩選暫停時也是如此。 如果篩選執行、暫停，然後再次執行，則暫停之後的第一個範例必須具有比暫停前最後一個樣本更大的時間戳記。

視您要捕捉的資料而定，可能會有適當的設定範例媒體時間。

如需詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 影片捕獲篩選](directshow-video-capture-filters.md)
</dt> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> <dt>

[寫入捕獲篩選器](writing-capture-filters.md)
</dt> </dl>

 

 



