---
description: 本主題說明如何在 Microsoft 媒體基礎中執行自訂媒體來源。
ms.assetid: 82db6f32-ad94-4563-b8bd-8a5072c5b221
title: 撰寫自訂媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e240277d5bbbabe5068f3a5f10bdb0312c29410def51bdced14715c1d3d68b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343188"
---
# <a name="writing-a-custom-media-source"></a>撰寫自訂媒體來源

本主題說明如何在 Microsoft 媒體基礎中執行自訂媒體來源。 它包含下列區段：

-   [建立簡報描述項](#creating-the-presentation-descriptor)
-   [啟動媒體來源](#starting-the-media-source)
    -   [尋求](#seeking)
-   [暫停媒體來源](#pausing-the-media-source)
-   [產生來源資料](#generating-source-data)
    -   [範例要求](#sample-requests)
    -   [配置範例](#allocating-samples)
    -   [資料流程中的間距](#gaps-in-the-stream)
-   [關閉媒體來源](#shutting-down-the-media-source)
-   [即時來源](#live-sources)
-   [相關主題](#related-topics)

## <a name="creating-the-presentation-descriptor"></a>建立簡報描述項

[**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)方法會傳回來源展示描述項的複本。 若要建立展示描述項，您必須知道來源內容中的資料流程數目，以及每個資料流程的可能格式。 針對每個資料流程，建立資料流程描述項，如下所示：

1.  建立媒體類型的陣列。 陣列中的每個媒體類型都代表資料流程可能的格式。 如需有關建立媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。
2.  呼叫 [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) 來建立資料流程描述項。 傳入媒體類型的陣列。 函數會傳回 [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) 指標。
3.  呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 來取得資料流程描述項的媒體類型處理常式。
4.  呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 來設定預設資料流程格式。 使用您在步驟1中建立的其中一種媒體類型。 一般而言，您應該使用具有最高品質的格式。
5.  （選擇性）在資料流程描述項上設定屬性。 如需適用于資料流程描述項的屬性清單，請參閱 [資料流程描述項屬性](stream-descriptor-attributes.md)。

現在建立簡報描述項：

1.  呼叫 [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) 並傳入資料流程描述項的陣列。 函數會傳回 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 指標。
2.  藉由呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 來選取一或多個資料流程，以選擇預設資料流程選取範圍。 預設設定中必須至少選取一個資料流程。
3.  （選擇性）在表示描述項上設定屬性。 如需適用于資料流程描述項的屬性清單，請參閱 [展示描述項屬性](presentation-descriptor-attributes.md)。

您應該在啟動時或來源已剖析足夠的來源資料來判斷內容之後，建立簡報描述項一次。 [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)方法應該會傳回展示描述項的複本。 若要建立複本，請呼叫 [**IMFPresentationDescriptor：： Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone)。 傳回復制可防止用戶端修改原始簡報描述項的狀態，例如屬性或資料流程選取專案。 不過，請注意， **Clone** 會建立淺層複製，因此用戶端可能會修改基礎資料流程描述項。

## <a name="starting-the-media-source"></a>啟動媒體來源

[**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)方法會啟動媒體來源，或搜尋至新的位置。 當先前狀態為 [已暫停] 或 [執行中]，並指定新的開始時間時， **開始** 的呼叫會導致 *搜尋* 。 否則， **start** 方法會 *啟動*。 當 **啟動** 作業完成時，傳送下列事件。

1.  針對每個新的資料流程傳送 [MENewStream](menewstream.md) 事件，也就是先前已取消選取且現在已選取的每個資料流程。 事件資料是資料流程的指標。
2.  針對每個先前選取且仍選取的資料流程傳送 [MEUpdatedStream](meupdatedstream.md) 事件。 事件資料是資料流程的指標。  (不會傳送已取消選取之資料流程的事件。 ) 
3.  如果來源正在搜尋，請傳送 [MESourceSeeked](mesourceseeked.md) 事件。 否則，請傳送 [MESourceStarted](mesourcestarted.md) 事件。 事件資料是 [**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法中所指定的開始時間。 針對 MESourceStarted 事件，如果開始時間是 VT \_ 空白，請在事件上設定 [**MF \_ 事件 \_ 來源 \_ 實際 \_ 開始**](mf-event-source-actual-start-attribute.md) 屬性。 屬性值是實際的開始時間。
4.  針對每個資料流程，如果來源正在搜尋，請傳送 [MEStreamSeeked](mestreamseeked.md) 事件。 否則，請傳送 [MEStreamStarted](mestreamstarted.md) 事件。 事件資料是開始時間。  (媒體來源可以呼叫資料流程的 [**IMFMediaEventGenerator：： QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent) 方法，將資料流程上的事件排入佇列。 ) 

取消選取資料流程時，會關閉資料流程。 資料流程不應該在該時間點將其他事件排在佇列中。

[**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)方法的時間格式是在 *pguidTimeFormat* 參數中提供。 標準時間格式（以 **GUID \_ Null** 表示）是 100-毫微秒單位。 媒體來源必須支援此時間格式。

### <a name="seeking"></a>尋求

搜尋時，要求的開始位置可能不會落在確切的取樣界限上。 此外，針對壓縮的內容，開始位置可能會落在主要畫面格之間。 資料流程應從所需的最早點傳遞範例，以在要求的開始位置產生未壓縮的範例。 針對影片，這表示從上一個主要畫面格開始。 管線負責從解碼器卸載額外的畫面格，以便在要求的時間開始播放。

來源事件中指定的開始時間 ([MESourceStarted](mesourcestarted.md)、 [MESourceSeeked](mesourceseeked.md)、 [MEStreamStarted](mestreamstarted.md)和 [MEStreamSeeked](mestreamseeked.md)) 是要求的開始時間 ([**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法) 指定的值，而不論實際的開始位置。

例如，假設影片串流的前幾個畫面有下列特性：



| 範例     | 1       | 2       | 3        | 4        |
|------------|---------|---------|----------|----------|
| Time       | 33毫秒 | 66毫秒 | 100毫秒 | 133毫秒 |
| 主要畫面格？ | 是     | 否      | 否       | 是      |



 

如果呼叫 [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法時的值為100毫秒，則來源需要輸出從畫面格1開始的影片（這段時間之前的第一個主要畫面格）。 啟動事件仍會指出事件資料中的100毫秒。

## <a name="pausing-the-media-source"></a>暫停媒體來源

[**IMFMediaSource：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)方法會暫停媒體來源。

當來源暫停時，資料流程可以建立新的範例，並將它們儲存在佇列中，但資料流程不會傳遞範例。 以下是此規則的一些例外狀況：

-   即時來源應該會在暫停時捨棄資料。
-   如果來源從網路取得資料，它可能會暫停伺服器。

如果用戶端在來源暫停時呼叫 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) ，要求也會排入佇列，直到再次啟動來源為止。 不應卸載要求。

只有啟動狀態才允許暫停。 否則， [**暫停**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) 應該會傳回 **MF \_ E 不正確 \_ \_ 狀態 \_ 轉換**。

## <a name="generating-source-data"></a>產生來源資料

媒體基礎使用 *提取模型*，這表示資料流程會產生並傳遞範例以回應管線的要求。 當媒體來源正在執行且已選取資料流程時，資料流程可以傳遞範例。 只有當用戶端要求新的範例時，資料流程才會傳遞資料。

### <a name="sample-requests"></a>範例要求

用戶端會藉由呼叫 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)來要求新的範例。 作業的順序如下：

1.  用戶端會呼叫 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)。 引數是用戶端用來追蹤要求之選擇性 *token* 物件的指標。 用戶端會執行權杖。 標記必須公開 **IUnknown** 介面。 用戶端也可以傳入 Null 指標，而不是權杖。
2.  如果用戶端提供權杖，則媒體資料流程會在權杖上呼叫 **AddRef** ，並將權杖放在先進先出佇列中。 方法會傳回，其餘的步驟則會以非同步方式發生。

3.  當有更多資料可用時，媒體資料流程會建立新的範例。  (此步驟會在下一節中詳細說明。 ) 
4.  媒體資料流程會從佇列提取第一個 token。
5.  如果 token 不是 **Null**，則媒體資料流程會在媒體範例上設定 [**MFSampleExtension \_ token**](mfsampleextension-token-attribute.md) 屬性。 屬性的值是 token 的指標。
6.  媒體資料流程會傳送 [MEMediaSample](memediasample.md) 事件。 事件資料是範例 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的指標。
7.  如果用戶端提供權杖，則媒體資料流程會在 token 物件上呼叫 **Release** 。

如果媒體資料流程無法完成用戶端的 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 要求，就會從佇列提取權杖，並在權杖上呼叫 **Release** ，但不會傳送 [MEMediaSample](memediasample.md) 事件。

用戶端可以使用權杖來追蹤要求的狀態。 當用戶端收到 [MEMediaSample](memediasample.md) 事件時，它可以從範例取得權杖，並將它與原始要求比對。 用戶端也可以使用權杖來偵測媒體來源是否已卸載要求。 如果權杖的參考計數為零，而媒體資料流程未傳送 MEMediaSample 事件，則表示要求已被捨棄。

此處所列的步驟假設 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法會實作為非同步作業。 如果方法是同步的，您就不需要將要求權杖放在佇列上。 但是，如果產生資料需要相當長的時間，建議使用非同步方法，例如，如果來源從位元組資料流程讀取資料。

資料流程負責緩衝處理 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)呼叫之間累積的任何資料。

當媒體資料流程到達資料流程的結尾時，它會在最後一個範例之後傳送 [MEEndOfStream](meendofstream.md) 事件。 在每個資料流程結束後，媒體來源會傳送 [MEEndOfPresentation](meendofpresentation.md) 事件。 當媒體資料流程傳送 MEEndOfStream 事件之後， [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法會傳回 **MF \_ E \_ 結束 \_ 的 \_ 資料流程** ，直到重新開機來源為止。

### <a name="allocating-samples"></a>配置範例

當資料流程準備好填滿暫止的範例要求時，它會建立新的範例，並將一或多個媒體緩衝區新增至範例。 如需有關建立媒體緩衝區的詳細資訊，請參閱 [媒體緩衝區](media-buffers.md)。

如果已知，資料流程必須設定時間戳記和持續時間。 時間戳記相對於來源。 在大部分情況下，內容的開頭會對應到時間戳記0。 例如，如果來源從媒體檔案讀取，則檔案的開頭會有時間戳記為零。

範例上的時間戳記不一定等於呈現時間。 媒體會話會從來源時間轉譯為呈現時間。 針對壓縮的資料，資料流程應該在開始時間之前從最接近的主要畫面格產生資料。 這可讓解碼器傳遞在要求的開始時間出現的畫面格。 否則，必須等到下列主要 ) 畫面格之後，才 (。

如果播放速率比1.0 更快或更慢，則管線會調整呈現時鐘的速率。 來源不會調整範例上的時間戳記。

來源可以設定屬性，以設定此範例的其他資訊。 如需範例屬性的清單，請參閱 [範例屬性](sample-attributes.md)。

### <a name="gaps-in-the-stream"></a>資料流程中的間距

如果資料流程包含明顯長度的間隙，建議資料流程傳送 [MEStreamTick](mestreamtick.md) 事件。 此事件會通知用戶端缺少範例。 事件資料是遺失範例的時間戳記，以 100-毫微秒單位 (**VT \_ I8**) 。 此事件可以儲存下游元件，使其無法等候不會抵達的範例。 資料流程可以視需要傳送任意數量的 MEStreamTick 事件，以跨越資料流程中的間距。

## <a name="shutting-down-the-media-source"></a>關閉媒體來源

當用戶端使用媒體來源完成時，它會呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)。 在這個方法內，媒體來源應該會中斷任何迴圈的參考計數。 一般而言，媒體來源和媒體串流之間會有迴圈參考。

如果您使用事件佇列來執行 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)，請在事件佇列上呼叫 [**IMFMediaEventQueue：： Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) 。 這個方法會關閉事件佇列，並對目前正在等候事件的任何呼叫端發出信號。

關機之後，來源上的所有方法都會傳回 **MF \_ E \_ 關機**，但 **IUnknown** 方法除外。

## <a name="live-sources"></a>即時來源

從 Windows 7 開始，媒體基礎會自動支援音訊和影片捕獲裝置。 若為影片，裝置必須在影片捕獲類別中提供內核串流 (KS) 迷你驅動程式。 媒體基礎使用 PnP 路徑來列舉裝置。 若是音訊，媒體基礎使用 Windows 多媒體裝置 (MMDevice) API 來列舉音訊端點裝置。 如果裝置符合這些條件，就不需要執行自訂媒體來源。

不過，您可能會想要為某些其他類型的裝置或其他即時資料源，執行自訂媒體來源。 即時來源與其他媒體來源之間只有幾個差異：

-   在 [**IMFMediaSource：： GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics) 方法中，傳回 **MFMEDIASOURCE \_ 為 \_ 即時** 旗標。
-   第一個範例的時間戳記應為零。
-   事件和串流狀態的處理方式與媒體來源相同，但暫停狀態除外。
-   暫停時，請勿將範例排在佇列中。 卸載任何在暫停時產生的資料。
-   即時來源通常不支援搜尋、反向播放或速率控制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體來源](media-sources.md)
</dt> <dt>

[教學課程：撰寫自訂媒體來源](tutorial--writing-a-custom-media-source.md)
</dt> </dl>

 

 



