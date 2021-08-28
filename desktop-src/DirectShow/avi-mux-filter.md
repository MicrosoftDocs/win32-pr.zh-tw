---
description: AVI Mux 篩選
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: AVI Mux 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f923ed944781bbaa36179b02db9022f38fc98ff6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478634"
---
# <a name="avi-mux-filter"></a>AVI Mux 篩選

AVI Mux 篩選器接受多個輸入資料流程，並將它們交錯成 AVI 格式。 篩選器會針對每個輸入資料流程使用不同的輸入圖釘，並針對 AVI 資料流程使用一個輸出圖釘。

影片捕獲或撰寫應用程式可以使用此篩選器，將檔案以 AVI 格式儲存至磁片。 篩選通常會連接到檔案 [寫入](file-writer-filter.md) 器篩選器，但它可以連接到任何輸入 Pin 支援 IStream 和 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的篩選。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>、ISpecifyPropertyPages | |輸入 Pin 媒體類型 |對應至舊樣式 FOURCC 或 MEDIATYPE_AUXLine21Data 的任何主要型別。  (需詳細資訊，請參閱 <a href="fourccmap.md"><strong>FOURCCMap 類別</strong></a>。 ) <ul><li>如果主要類型為 MEDIATYPE_Audio，則格式必須為 FORMAT_WaveFormatEx。</li><li>如果主要類型為 MEDIATYPE_Video，則格式必須為 FORMAT_VideoInfo 或 FORMAT_DvInfo。</li><li>如果主要類型為 MEDIATYPE_Interleaved，則格式必須為 FORMAT_DvInfo。</li></ul> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、IPropertyBag、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 |MEDIATYPE_Stream，MEDIASUBTYPE_Avi | |輸出 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |CLSID_AviDest | |屬性頁 CLSID |CLSID_AviMuxProptyPage，CLSID_AviMuxProptyPage1 | |可執行檔 |qcap.dll | | <a href="merit.md">業績</a> |MERIT_DO_NOT_USE | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>備註

下列備註說明 AVI Mux 篩選功能的各種層面。

釘選

建立 AVI Mux 篩選器時，它會有一個輸入的 pin。 當每個輸入 pin 連線時，篩選準則會建立新的輸入 pin。

資料流程屬性

輸入 pin 支援 IPropertyBag 介面，以便在個別資料流程上設定屬性。 目前已定義下列屬性：



| 屬性 | 描述                                                           |
|----------|-----------------------------------------------------------------------|
| NAME     | 資料流的名稱。 這個屬性會寫入為 `'strn'` 區塊。 |



 

如果篩選器正在執行或已暫停，IPropertyBag：： Write 方法會傳回 VFW \_ E \_ 錯誤的 \_ 狀態。

畫面播放速率

如果上游篩選未在 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構的 **AvgTimePerFrame** 成員中指定畫面播放速率，則 AVI Mux 會使用第一個影片畫面上的時間戳記。 AVI 檔案格式不支援可變的畫面播放速率。

捨棄的畫面格

AVI Mux 篩選器會根據每個樣本的媒體時間（如果有的話）來計算已卸載的框架，或使用範例的時間戳記。 它會針對每個已捨棄的框架寫入長度為零的索引項目目。

IMediaSeeking

AVI Mux 篩選器會實 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面，如下所示：

-   [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition)方法會傳回多工處理的目前進度。 如果您正在轉碼檔案 (慢于即時) ，此值會比篩選 Graph 管理員所傳回的值更準確。 如需詳細資訊，請參閱 GetCurrentPosition 參考頁面的備註一節。
-   [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)方法會查詢每個上游篩選器，並傳回最長資料流程的持續時間。 如果這些篩選準則中有任何一個失敗 (或不支援 IMediaSeeking) ，則 AVI Mux 會傳回失敗碼，並在找到的最長持續時間內填入 *pDuration* 參數。 不過，在此情況下， *pDuration* 的值不一定是最長輸入資料流程的長度。
-   AVI Mux 不會執行 GetStopPosition、GetPositions、GetAvailable、GetRate 或 GetPreroll 方法;也不會執行任何 Set \* 方法進行搜尋。

AVI 2.0 檔案格式延伸模組

DirectShow 目前支援下列 AVI 2.0 檔案格式延伸模組：

-    (大於 1 GB 的 AVI 檔案大小增加) 
-   階層式索引編制

如需詳細資訊，請參閱 OpenDML AVI M-JPEG 檔案格式 Subcommittee 所發佈之「OpenDML AVI 檔案格式延伸模組」的1.02 版。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



