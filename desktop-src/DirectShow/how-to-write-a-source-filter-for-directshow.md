---
description: 本主題說明如何撰寫 DirectShow 的自訂來源篩選。
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: 如何為 DirectShow 撰寫來源篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ea6821dc7d56f2628ce68e7320e5e76b2c1643978e68287d434b7a111cbbd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043238"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>如何為 DirectShow 撰寫來源篩選

本主題說明如何撰寫 DirectShow 的自訂來源篩選。

> [!Note]  
> 本主題僅描述推送來源;它不會描述提取來源（例如，非同步讀取器篩選器）或連接到提取來源的分隔器篩選。 如需 *推送* 和 *提取* 來源之間的差異，請參閱 [篩選開發人員的資料 Flow](data-flow-for-filter-developers.md)。

 

## <a name="the-directshow-streaming-model"></a>DirectShow 串流模型

當您撰寫來源篩選器時，請務必瞭解推播來源與即時來源的內容不同。 即時來源會從某個外部來源（例如相機或網路串流）取得資料。 一般情況下，即時來源無法控制傳入資料的速率。 如果下游篩選器的資料不夠快，則來源需要卸載範例。

但推送來源不必是即時來源。 例如，推送來源可以從本機檔案讀取資料。 在這種情況下，下游轉譯器篩選器會根據參考時鐘和取樣時間戳記，判斷其從來源取用資料的速度。 來源篩選器會儘快傳遞範例，但實際的資料流程會受到轉譯器的限制。 [篩選器開發人員的資料 Flow](data-flow-for-filter-developers.md)會描述控制資料流程的機制。

來源篩選器上的每個輸出釘選都會建立一個稱為 *串流執行緒* 的執行緒。 Pin 會在串流處理執行緒上提供範例。 一般而言，所有的解碼、處理和轉譯都會發生在此執行緒上，不過某些下游篩選器可能會建立額外的執行緒，以將其輸出範例排入佇列。

串流執行緒會使用下列結構執行迴圈：

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

如果沒有可用的範例，步驟1會封鎖，直到範例可供使用為止。 步驟4也可以封鎖;例如，它可以在圖形暫停時封鎖。

迴圈會儘快執行，但受限於轉譯器篩選器轉譯每個樣本的速度。 假設篩選圖形具有參考時鐘，則速率取決於樣本上的呈現時間。 如果沒有參考時鐘，轉譯器會儘快取用樣本。

## <a name="using-csource-and-csourcestream"></a>使用 CSource 和 CSourceStream

DirectShow 基類包含兩個支援推送來源的類別： [**CSource**](csource.md)和 [**CSourceStream**](csourcestream.md)。

-   [**CSource**](csource.md) 是篩選的基類，並會執行 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面。
-   [**CSourceStream**](csourcestream.md) 是輸出圖釘的基類，並會執行 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面。

### <a name="output-pins"></a>輸出圖釘

來源篩選器可以有一個以上的輸出圖釘。 在篩選器的函式方法中，建立一或多個衍生自 [**CSourceStream**](csourcestream.md) 的 pin (每個輸出資料流程) 一個 pin。 您不需要儲存釘選的指標;pin 會在建立時自動將自己新增至篩選準則。

### <a name="output-formats"></a>輸出格式

輸出圖釘會使用下列 [**CSourceStream**](csourcestream.md) 方法來處理格式的協商：



| 方法                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetMediaType**](csourcestream-getmediatype.md)     | 從輸出圖釘取得媒體類型。 <br/> Pin 必須至少提議一個媒體類型，因為下游篩選器可能不會建議任何類型。 在大部分情況下，下游篩選器會是一個解碼器或轉譯器，視來源篩選器是否提供壓縮或未壓縮的資料而定。 轉譯器篩選器通常需要完整的媒體類型，其中包含轉譯資料流程所需的所有格式資訊。 若為解碼器，媒體類型中所需的資訊數量，會非常依賴編碼格式。<br/> |
| [**CheckMediaType**](csourcestream-checkmediatype.md) | 檢查輸出釘選是否接受指定的媒體類型。 覆寫這個方法是選擇性的，視您執行 [**GetMediaType**](csourcestream-getmediatype.md)的方式而定。                                                                                                                                                                                                                                                                                                                                                                                                         |



 

[**GetMediaType**](csourcestream-getmediatype.md)方法超載：

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) 接受單一參數，也就是 [**CMediaType**](cmediatype.md) 物件的指標。
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) 接受索引變數和 [**CMediaType**](cmediatype.md) 物件的指標。

如果來源篩選的輸出 pin 只支援一個媒體格式，您應該覆寫 (1) ，以使用該格式來初始化 [**CMediaType**](cmediatype.md) 物件。 保留 (2) 的預設值，並保留 [**CheckMediaType**](csourcestream-checkmediatype.md)的預設執行。

如果 pin 支援一種以上的格式，請覆寫 (2) 。 根據索引變數的值，初始化 [**CMediaType**](cmediatype.md) 物件。 Pin 應會以排序清單的形式傳回格式。 在此情況下，您也必須覆寫 [**CheckMediaType**](csourcestream-checkmediatype.md) ，以根據您的格式清單來檢查媒體類型。

針對未壓縮的影片格式，請記住下游篩選器可以使用各種 stride 值來建議格式。 您的篩選準則應該接受任何有效的 stride 值。 如需詳細資訊，請參閱 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)。

您也必須覆寫純虛擬 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) 方法。 您可以使用這個方法來設定範例緩衝區的大小。

### <a name="streaming"></a>串流

[**CSourceStream**](csourcestream.md)類別會建立 pin 的串流執行緒。 執行緒程式是在 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 方法中執行。 這個方法會呼叫衍生類別必須覆寫的純虛擬 [**CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md) 方法。 此方法是 pin 將資料填入緩衝區的位置。 例如，如果您的篩選器提供未壓縮的影片，這就是您要在其中繪製影片畫面的位置。

當篩選暫停或停止時，基類會自動啟動，並且在正確的時間停止執行緒迴圈。 發生這種情況時， [**CSourceStream**](csourcestream.md) 類別會呼叫一些方法來通知您的衍生類別：

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

如果您需要新增任何特殊處理，可以覆寫這些方法。 否則，預設的實值只會傳回 **S \_ OK**。

## <a name="seeking"></a>尋求

如果您的來源篩選具有一個輸出釘選，您可以使用 [**CSourceSeeking**](csourceseeking.md) 類別做為實作為搜尋起點的起點。 從 [**CSourceStream**](csourcestream.md) 和 **CSourceSeeking** 繼承您的 pin 類別。

> [!Note]  
> 如果篩選具有多個輸出釘選，則不建議使用 [**CSourceSeeking**](csourceseeking.md) 。 主要的問題是只有一個 pin 應該回應搜尋要求。 這通常需要 pin 和篩選之間的通訊。

 

[**CSourceSeeking**](csourceseeking.md)類別會管理播放速率、開始時間、停止時間和持續時間。 您的衍生類別應該設定初始停止時間和持續時間。 每當其中一個值變更時，就會適當地呼叫 [**CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)、 [**CSourceSeeking：： ChangeStart**](csourceseeking-changestart.md)或 [**CSourceSeeking：： ChangeStop**](csourceseeking-changestop.md) 方法。 這些方法都是純虛擬方法。 衍生的 pin 類別會覆寫這些方法以執行下列動作：

1.  在下游 pin 上呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 。 這會導致下游篩選器發行它們所持有的範例，並拒絕新的範例。
2.  呼叫 [**CSourceStream：： stop**](csourcestream-stop.md) 以停止串流處理執行緒。 來源篩選器會暫停產生新的資料。
3.  在下游 pin 上呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 。 這會通知下游篩選器接受新的資料。
4.  以新的開始和停止時間和速率呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 。
5.  在下一個範例中，設定 [不中斷] 屬性。

如需詳細資訊，請參閱 [在來源篩選中支援搜尋](supporting-seeking-in-a-source-filter.md)。

如果您的篩選準則支援搜尋，則資料流程位置現在與展示時間無關。 搜尋之後，時間戳記會重設為零。 時間戳記的一般公式為：

-   範例開始時間 = 經過時間/播放速率
-   範例結束時間 = 取樣開始時間 + 每個畫面格/播放速率 (時間) 

*經過的時間* 是從篩選開始執行或自上次搜尋命令以來經過的時間。

### <a name="time-formats-for-seeking"></a>搜尋的時間格式

依預設，搜尋命令的單位為 100-毫微秒。 來源篩選器可支援其他時間格式，例如依框架編號搜尋。 每一段時間的格式都是由 GUID 來識別;請參閱 [**時間格式 guid**](time-format-guids.md)。

若要支援其他時間格式，您必須在輸出釘選上執行下列方法：

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

如果應用程式設定新的時間格式，則會根據新的時間格式來解讀 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法中的所有位置參數。 例如，如果時間格式是畫面格， [**IMediaSeeking：： GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法必須傳回框架中的持續時間。

在實務上，少數 DirectShow 篩選準則支援額外的時間格式，因此，少數 DirectShow 的應用程式會使用這項功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寫入來源篩選](writing-source-filters.md)
</dt> </dl>

 

 




