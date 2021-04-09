---
description: 在 DirectShow 中使用 DMOs
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: 在 DirectShow 中使用 DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115769"
---
# <a name="using-dmos-in-directshow"></a>在 DirectShow 中使用 DMOs

以 DirectShow 為基礎的應用程式可以使用篩選圖形中的 DMOs，[透過 []](dmo-wrapper-filter.md) 此篩選準則會匯總一，並處理所有使用 SQL-DMO 的詳細資料，例如，將資料傳入和傳出、配置 [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) 物件等等。

因為是由篩選準則來匯總，所以應用程式可以查詢此篩選器中的任何 COM 介面。 但是，應用程式應該讓篩選器處理該的所有串流作業。 例如，請勿設定媒體類型、處理任何緩衝區、排清、鎖定，以及啟用或停用品質控制，或設定影片優化。

如果您知道您想要使用之特定的) 的類別識別碼 (CLSID，您可以使用該的

1.  呼叫 **CoCreateInstance** 以建立 [的] 包裝函式篩選。
2.  查詢 [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) 介面的 sql-dmo 包裝函式篩選。
3.  呼叫 [**IDMOWrapperFilter：： Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) 方法。 指定 SQL-DMO 的 CLSID 和此的類別的 GUID。 For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).

下列程式碼顯示這些步驟：


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



[**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)函式會列舉登錄中的 DMOs。 此函式會使用用於 DirectShow 篩選器的不同分類 Guid 集合。

**使用系統裝置列舉值搭配 DMOs**

您可以使用 [系統裝置](system-device-enumerator.md)列舉值來列舉 **DMOEnum** 方法所支援的任何 sql-dmo 類別，而不是直接建立一個。 當系統裝置枚舉器列舉特定的 DirectShow 篩選類別時，也會包含 DMOs。 下表顯示的是 SQL-DMO 類別和 DirectShow 類別之間的對應。



|                             |                                |
|-----------------------------|--------------------------------|
| SQL-DMO 類別                | DirectShow 對等          |
| DMOCATEGORY \_ 音訊 \_ 編碼器 | CLSID \_ AudioCompressorCategory |
| DMOCATEGORY \_ 音訊 \_ 解碼器 | CLSID \_ LegacyAmFilterCategory  |
| DMOCATEGORY \_ 影片 \_ 編碼器 | CLSID \_ VideoCompressorCategory |
| DMOCATEGORY \_ 影片 \_ 解碼器 | CLSID \_ LegacyAmFilterCategory  |



 

系統裝置列舉值會傳回一份標記物件清單。 如果標記法代表的是，則 **IMoniker：： BindToObject** 方法會自動建立 sql-dmo 包裝函式篩選器，並將它初始化為該。 這樣一來，就會對應用程式透明說出一種。 如需使用系統裝置列舉值的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。

**限制**

在 DirectShow 中使用 DMOs 時，有一些限制：

-   SQL-DMO 包裝函式篩選不支援具有零個輸入的 DMOs、多個輸入或零個輸出。
-   SQL-DMO 包裝函式篩選器上的所有 pin 連接都會使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。
-   DirectShow 編輯服務不支援以 SQL-DMO 為基礎的效果或轉換。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DMOs](using-dmos.md)
</dt> </dl>

 

 



