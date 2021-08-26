---
description: 在 DirectShow 中使用 DMOs
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: 在 DirectShow 中使用 DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d056d22e5e9b42795cbe95ce676ac293605453200e0a691d4f0d00374e94cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078648"
---
# <a name="using-dmos-in-directshow"></a>在 DirectShow 中使用 DMOs

以 DirectShow 為基礎的應用程式可以透過[DMO 包裝](dmo-wrapper-filter.md)函式篩選，在篩選圖形中使用 DMOs。 此篩選準則會匯總 DMO，並處理所有使用 DMO 的詳細資料，例如將資料傳入和傳出 DMO、配置 [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer)物件等等。

由於 DMO 是由篩選準則匯總，因此應用程式可以查詢 DMO 所公開之任何 COM 介面的篩選。 但是，應用程式應該讓篩選器處理 DMO 上的所有串流作業。 例如，請勿設定媒體類型、處理任何緩衝區、清除 DMO、鎖定 DMO、啟用或停用品質控制，或設定影片優化。

如果您知道您想要使用之特定 DMO 的 (CLSID) 的類別識別碼，您可以使用該 DMO 初始化 DMO 包裝函式篩選，如下所示：

1.  呼叫 **CoCreateInstance** 以建立 DMO 包裝函式篩選。
2.  查詢 [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)介面的 DMO 包裝函式篩選。
3.  呼叫 [**IDMOWrapperFilter：： Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) 方法。 指定 DMO 的 CLSID 以及 DMO 類別的 GUID。 如需 DMO 類別的清單，請參閱[DMO guid](dmo-guids.md)。

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



[**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)函式會列舉登錄中的 DMOs。 此函式會使用用於 DirectShow 篩選器的不同分類 guid 集合。

**使用系統裝置列舉值搭配 DMOs**

您可以使用 [系統裝置](system-device-enumerator.md)列舉值來列舉 **DMOEnum** 方法所支援的任何 DMO 類別，而不是直接建立 DMO。 系統裝置枚舉器在列舉某些 DirectShow 篩選準則分類時，也會包含 DMOs。 下表顯示 DMO 分類與 DirectShow 類別之間的對應。



| 標籤 | 值 |
|-----------------------------|--------------------------------|
| DMO類別                | DirectShow等效          |
| DMOCATEGORY \_ 音訊 \_ 編碼器 | CLSID \_ AudioCompressorCategory |
| DMOCATEGORY \_ 音訊 \_ 解碼器 | CLSID \_ LegacyAmFilterCategory  |
| DMOCATEGORY \_ 影片 \_ 編碼器 | CLSID \_ VideoCompressorCategory |
| DMOCATEGORY \_ 影片 \_ 解碼器 | CLSID \_ LegacyAmFilterCategory  |



 

系統裝置列舉值會傳回一份標記物件清單。 如果標記代表 DMO， **IMoniker：： BindToObject** 方法會自動建立 DMO 包裝函式篩選器，並使用該 DMO 加以初始化。 因此，DMO 涉及的事實對應用程式而言是透明的。 如需使用系統裝置列舉值的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。

**限制**

在 DirectShow 中使用 DMOs 時，有一些限制：

-   DMO 包裝函式篩選不支援具有零個輸入的 DMOs、多個輸入或零個輸出。
-   DMO 包裝函式篩選器上的所有 pin 連接都會使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)介面。
-   DirectShow編輯服務不支援以 DMO 為基礎的效果或轉換。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DMOs](using-dmos.md)
</dt> </dl>

 

 



