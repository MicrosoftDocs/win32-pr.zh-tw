---
description: 設定 Graph 時鐘
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: 設定 Graph 時鐘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab93fcefe4ba88aa7724bf59b775c493313783b2f4ad3801925e16b9a1818c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904138"
---
# <a name="setting-the-graph-clock"></a>設定 Graph 時鐘

當您建立篩選圖形時，Graph 管理員的篩選器會自動為圖形選擇參考時鐘。 圖形中的所有篩選都會同步處理到參考時鐘。 尤其是，轉譯器篩選器會使用參考時鐘來判斷每個樣本的呈現時間。

應用程式通常不會有理由覆寫 Graph Manager 的參考時鐘選擇的篩選器。 不過，您可以在篩選 Graph 管理員上呼叫 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)方法來這麼做。 這個方法會採用時鐘 **IReferenceClock** 介面的指標。 當圖形停止時，呼叫方法。

如果篩選準則提供時鐘，您可以藉由呼叫篩選準則的 **QueryInterface** 來取得 **IReferenceClock** 指標。 或者，只要您的外部時鐘實 **IReferenceClock**，您就可以執行篩選不提供的外部參考時鐘。 下列範例顯示如何指定時鐘：


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



此範例假設 CreateMyPrivateClock 是應用程式定義的函式，它會建立時鐘並傳回 **IReferenceClock** 指標。

您也可以使用 **Null** 值呼叫 **SetSyncSource** ，將篩選圖形設定為不使用時鐘執行。 如果沒有時鐘，圖形會儘快執行。 如果沒有時鐘，轉譯器篩選不會等候樣本的呈現時間。 相反地，它們會在每個範例抵達時立即轉譯。 如果您想要快速地處理資料，而不是即時預覽，則將圖形設定為在沒有時鐘的情況下執行會很有用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本 DirectShow 工作](basic-directshow-tasks.md)
</dt> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



