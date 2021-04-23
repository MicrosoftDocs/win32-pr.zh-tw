---
description: SQL-DMO 包裝函式篩選
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: SQL-DMO 包裝函式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29c5b86bdff4a215ec2ef5854d09a1f842dbf0e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908626"
---
# <a name="dmo-wrapper-filter"></a>SQL-DMO 包裝函式篩選

SQL-DMO 包裝函式篩選器可讓 DirectShow 應用程式在篩選圖形中使用 [DirectX 媒體物件](directx-media-objects.md) (的) 。 篩選準則會包裝，並處理所有使用 SQL-DMO 的詳細資料，例如將資料傳入和傳送。 此外，篩選準則會匯總]，讓應用程式可以查詢任何適用于 SQL-DMO 所公開之 COM 介面的篩選。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)、 [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| 輸入 Pin 媒體類型                    | 請參閱備註                                                                                                                                                                                                                                        |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| 輸出 Pin 媒體類型                   | 請參閱備註                                                                                                                                                                                                                                        |
| 輸出 Pin 介面                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | CLSID \_ DMOWrapperFilter                                                                                                                                                                                                                            |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                                                                                                                                   |
| 可執行檔                               | Qasf.dll                                                                                                                                                                                                                                           |
| [優點](merit.md)                       | 請參閱備註                                                                                                                                                                                                                                        |
| [篩選準則分類](filter-categories.md) | 請參閱備註                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>備註

### <a name="limitations"></a>限制

SQL-DMO 包裝函式有下列限制：

-   它不支援 DMOs 包含零個輸入、多個輸入或零個輸出。  (它確實支援具有一個輸入和多個輸出的 DMOs。 ) 
-   它不支援自訂傳輸。 所有資料傳輸都是透過 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面完成。
-   它不會使用 **IMediaObjectInPlace** 介面;所有處理都是使用 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 方法來完成。

### <a name="pins"></a>釘選

針對每個輸入資料流程，此篩選準則會建立對應的輸入 pin。 針對每個輸出資料流程，它會建立對應的輸出圖釘。 每個 pin 所支援的媒體類型取決於 SQL-DMO

### <a name="encoder-interfaces"></a>編碼器介面

如果 SQL-DMO 是影片編碼器或音訊編碼器，輸出圖釘會公開 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面。 如果 SQL-DMO 是影片編碼器，輸出釘選也會公開 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面。 在這兩種情況下，如果 SQL-DMO 支援介面，則釘選會委派給 SQL-DMO。 否則，pin 會提供自己的實作為。

### <a name="streaming"></a>串流

篩選器會使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面來處理所有串流處理。 它不支援 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 連接。 篩選準則只會在 IMediaObject 接收來自上游 (的資料時（包含) 的資料流程結束通知）時，才會呼叫 [**：:P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) 。 因此，它不支援 DMOs 為零的輸入資料流程。

### <a name="seeking"></a>尋求

所有搜尋要求都會透過的第一個輸入 pin，傳遞給您的上游篩選器。 針對多個輸出 DMOs，這表示上游篩選器可能會在應用程式搜尋圖形時收到多個搜尋要求。

### <a name="merit"></a>優點

DirectShow 會為所有 DMOs 指派預設的 [ **\_ 一般** ] + [0x800] 值。 此值落在 **慣用 \_ 標準** 和 **\_ 慣用** 的範圍之間。 「解碼」篩選器通常會有 **「 \_ 正常**」的價值。 因此，篩選圖形管理員通常會在一個解碼篩選器上選取一種， 若要覆寫預設的 [使用] 值，請將登錄專案新增至 HKEY \_ 類別 \_ 根目錄 CLSID 中的 sql-dmo 登錄機碼 \\ 。 包含名為「「有」值的 **DWORD** 值，其值會指定「業績」。

### <a name="category"></a>類別

在任何類別中，就不會將它本身顯示為 [i] 包裝函式篩選。 當它換行時，它會出現在 [DirectShow] 類別中，並對應至 [中] 的 [名稱]。

### <a name="buffers"></a>緩衝區

SQL-DMO 包裝函式篩選會將媒體緩衝區傳遞給用來公開 [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) 介面的]。

在 Windows Vista 或更新版本中，媒體緩衝區也會公開 IServiceProvider 介面。 您可以使用這個介面來取得與緩衝區相關聯之媒體範例的指標。 使用服務識別碼 **IID \_ IMediaSample**。 SQL-DMO 可以使用媒體範例的 [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) 介面來設定範例上的交錯旗標。 下列程式碼顯示如何取得媒體範例的指標：


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



如需有關每個範例交錯旗標的詳細資訊，請參閱 [**AM \_ Sample2.xml \_ 屬性結構**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)。

### <a name="quality-control"></a>品質控制

如果 SQL-DMO 公開了 [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) 介面，則篩選會將其輸出圖釘上的 [**IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 呼叫轉譯為上的 [**IDMOQualityControl：： SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) 呼叫。 **SetNow** 的 *rtNow* 參數會計算為 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構的 **時間戳記** 和 **晚期** 成員的總和。

### <a name="using-the-fiter-in-graphedit"></a>在 GraphEdit 中使用 Fiter

在 GraphEdit 中，SQL-DMO 包裝函式篩選不會出現在自己的名稱下。 相反地，每個註冊的每個類型都會列在適當的篩選準則類別之下。 當您透過 [ **插入篩選器** ] 對話方塊來新增時，GraphEdit 會建立一個 []，並將它設定為使用該。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[DirectX 媒體物件](directx-media-objects.md)
</dt> </dl>

 

 
