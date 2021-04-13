---
description: 媒體接收器是接收媒體資料的管線物件。
ms.assetid: a0fbce1b-0a16-4449-9eca-906fd9056a1c
title: 媒體接收器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9394cbfd49a631d59b9296202a2b6ca7a868869
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321475"
---
# <a name="media-sinks"></a>媒體接收器

*媒體接收器* 是接收媒體資料的管線物件。 媒體接收器是一或多個媒體資料流程的目的地。 媒體接收器分為兩個一般類別：

-   轉譯 *器是顯示* 播放資料的媒體接收器。 增強型影片轉譯器 (EVR) 會顯示影片畫面，而音訊轉譯器會透過音效卡或其他音訊裝置播放音訊串流。

-   *保存接收器* 是將資料寫入檔案或其他儲存體的媒體接收器。

兩者之間的主要差異在於，封存接收不會以固定的播放速率取用資料。 相反地，它會以最快的速度來寫入所收到的資料。

媒體接收器會公開 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面。 每個媒體接收都包含一或多個 *串流接收器*。 每個資料流程接收都會接收一個資料流程中的資料。 資料流程接收會公開 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面。 一般來說，應用程式不會直接建立媒體接收器。 相反地，應用程式會建立一個或多個啟用物件，媒體會話會使用這些物件來建立接收器。 接收上的所有其他作業都是由媒體會話處理，而應用程式不會呼叫媒體接收或任何資料流程接收上的任何方法。 如需啟用物件的詳細資訊，請參閱 [啟用物件](activation-objects.md)。

如果您要撰寫自訂媒體接收，或是想要直接使用媒體接收器而不使用媒體會話，請閱讀本主題的其餘部分。

-   [串流接收器](#stream-sinks)
-   [簡報時鐘](#presentation-clock)
-   [資料流程格式](#stream-formats)
-   [資料流程](#data-flow)
-   [標記](#markers)
-   [狀態變更](#state-changes)
-   [敲定](#finalizing)
-   [關閉](#shutting-down)
-   [媒體接收器介面](#media-sink-interfaces)
-   [資料流程接收介面](#stream-sink-interfaces)
-   [資料流程接收事件](#stream-sink-events)
-   [相關主題](#related-topics)

## <a name="stream-sinks"></a>串流接收器

媒體接收器可以有固定數目的資料流程接收器，也可以支援新增和移除資料流程接收。 如果有固定的資料流程接收數目， [**IMFMediaSink：： GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) 方法會傳回 MEDIASINK \_ 固定 \_ 資料流程旗標。 否則，您可以新增和移除資料流程接收。 若要加入新的資料流程接收，請呼叫 [**IMFMediaSink：： AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)。 若要移除資料流程接收，請呼叫 [**IMFMediaSink：： RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink)。 MEDIASINK \_ 固定 \_ 資料流程旗標表示媒體接收器不支援這兩種方法。  (它可能會支援一些其他方式來設定資料流程的數目，例如，在建立接收器時設定初始化參數。 ) 資料流程接收清單的順序。 若要依索引值列舉它們，請呼叫 [**IMFMediaSink：： GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) 方法。

資料流程接收也有識別碼。 串流識別碼在媒體接收器中是唯一的，但不需要連續。 根據媒體接收，資料流程識別碼可能會有一些與內容相關的意義。 例如，封存接收可能會將串流識別碼寫入檔案標頭。 否則，它們是任意的。 若要依識別碼取得資料流程接收，請呼叫 [**IMFMediaSink：： GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid)。

## <a name="presentation-clock"></a>簡報時鐘

媒體接收器取用樣本的速率是由 [呈現時鐘](presentation-clock.md)來控制。 媒體會話會透過呼叫媒體接收器的 [**IMFMediaSink：： SetPresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock) 方法，來選取簡報時鐘，並在媒體接收器上設定它。 您必須在媒體接收器上設定簡報時鐘，才能開始串流。 每個媒體接收器都需要簡報時鐘才能執行。 媒體接收器會使用簡報時鐘進行兩個用途：

-   在串流啟動或停止時接收通知。 媒體接收器會透過 [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) 介面接收這些通知，所有媒體接收都必須執行這些通知。

-   判斷它應該呈現範例的時機。 當媒體接收器收到新的範例時，它會從範例取得時間戳記，並嘗試在該呈現時間轉譯樣本。

簡報時鐘衍生自另一個物件（稱為「 *展示時間來源*」）的時鐘時間。 展示時間來源會公開 [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) 介面。 有些媒體接收器可以存取精確的時鐘，因此會公開此介面。 這表示媒體接收器可能會根據自己的時鐘所提供的時間來排定樣本。 不過，媒體接收器無法假設這是如此。 無論呈現時鐘是由媒體接收器本身或其他時鐘驅動，都必須一律使用呈現時鐘的時間。

如果媒體接收器無法以其本身的時鐘來比對速率，則 [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) 方法會傳回 MEDIASINK \_ 不 \_ 符合 \_ 時鐘旗標。 如果出現此旗標，且簡報時鐘使用不同的呈現時間來源，則媒體接收器的執行效能可能不佳。 例如，播放期間可能會有問題。

*Rateless* 接收是一個媒體接收，會忽略樣本上的時間戳記，並在每個範例抵達時立即取用資料。 Rateless 媒體接收器會傳回 \_ [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) 方法中的 MEDIASINK rateless 旗標。 此旗標通常會套用至封存接收。 如果管線中的每個媒體接收器都 rateless，媒體會話就會使用特殊的 rateless 呈現頻率。 當接收取用樣本時，此時鐘的執行速度很快。

## <a name="stream-formats"></a>資料流程格式

在媒體接收器可以接收範例之前，用戶端必須先設定資料流程接收上的媒體類型。 若要設定媒體類型，請呼叫串流接收器的 [**IMFStreamSink：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler) 方法。 這個方法會傳回 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面的指標。 您可以使用此介面來取得慣用媒體類型的清單、取得目前的媒體類型，以及設定媒體類型。

若要取得慣用媒體類型的清單，請呼叫 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex)。 慣用的型別應做為用戶端的提示。 清單可能不完整或包含部分媒體類型。 部分媒體類型是指沒有描述有效格式所需的所有屬性。 例如，部分影片類型可能會指定色彩空間和位深度，而不是影像寬度或高度。 部分音訊類型可能會指定壓縮格式和取樣率，但不能指定音訊聲道數目。

若要取得資料流程接收器目前的媒體類型，請呼叫 [**IMFMediaTypeHandler：： GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype)。 第一次建立資料流程接收時，可能會有已設定的預設媒體類型，或在用戶端設定一個之前，它可能沒有任何媒體類型。

若要設定媒體類型，請呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype)。 某些資料流程接收可能不支援在設定之後變更類型。 因此，在設定媒體類型之前先測試它很有用。 若要測試媒體接收器是否接受媒體類型， (不將類型設定) ，請呼叫 [**IMFMediaTypeHandler：： IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported)。

## <a name="data-flow"></a>資料流程

媒體接收器使用 *提取模型*，這表示資料流程會在需要時接收資料。 用戶端應該及時回應，以避免任何瑕疵。

有些媒體接收器支援 *prerolling*。 Prerolling 是在簡報時鐘開始之前，將資料提供給媒體接收器的程式。 如果媒體接收器支援 prerolling，則媒體接收器會公開 [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) 介面，而 [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) 方法會傳回 MEDIASINK 可以預先建立 \_ 旗標 \_ 。 Prerolling 可確保媒體接收器準備好在簡報時鐘開始時顯示第一個範例。 如果媒體接收器支援，則建議用戶端一律為預先執行，因為它可能會在播放期間防止瑕疵或間距。

傳送至媒體接收器的資料流程如下所示：

1.  用戶端會設定媒體類型和表示時鐘。 媒體接收器會向簡報時鐘註冊本身，以接收時鐘狀態變更的通知。
2.  （選擇性）用戶端查詢 [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)。 如果媒體接收器公開此介面，用戶端會呼叫 [**IMFMediaSinkPreroll：： NotifyPreroll**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasinkpreroll-notifypreroll)。 否則，用戶端會跳到步驟5。
3.  每個資料流程接收都會傳送一個或多個 [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) 事件。 為了回應每個事件，用戶端會取得該資料流程的下一個範例資料，並呼叫 [**IMFStreamSink：:P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample)。
4.  當每個串流接收收到足夠的預先產生資料時，它會傳送 [MEStreamSinkPrerolled](mestreamsinkprerolled.md) 事件。
5.  用戶端會呼叫 [**IMFPresentationClock：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) 來啟動簡報時鐘。
6.  簡報時鐘會藉由呼叫 [**IMFClockStateSink：： OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)，通知媒體接收器正在啟動時鐘。
7.  為了取得更多資料，每個資料流程接收都會傳送 [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) 事件。 為了回應每個事件，用戶端會取得下一個範例，並呼叫 [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample)。 此步驟會重複，直到簡報結束為止。

大部分的媒體接收器都會以非同步方式處理範例，因此串流接收一次可以傳送一個以上的範例要求。

在串流處理期間，用戶端可以隨時呼叫 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 和 [**IMFStreamSink：： Flush**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-flush) 。 下一節將說明標記。 清除會導致串流接收卸載已排入佇列但尚未轉譯的任何範例。

## <a name="markers"></a>標記

標記提供一種方式，讓用戶端表示資料流程中的特定點。 標記是由下列資訊所組成：

-   標記類型，定義為 [**MFSTREAMSINK \_ 標記 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfstreamsink_marker_type) 列舉的成員。
-   與標記相關聯的資料。 資料的意義取決於標記類型。 某些標記類型沒有資料。
-   用戶端本身使用的選擇性資料。

為了放置標記，用戶端會呼叫 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)。 資料流程接收會完成處理 **PlaceMarker** 呼叫之前所收到的任何範例，然後傳送 [MEStreamSinkMarker](mestreamsinkmarker.md) 事件。

大部分的媒體接收器都會保留擱置範例的佇列，而這些範例會以非同步方式處理。 標記事件必須使用範例處理進行序列化，因此媒體接收器應該將標記放置在相同的佇列中。 例如，假設用戶端會呼叫下列方法：

1.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (範例 \# 1) 
2.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (範例 \# 2) 
3.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (標記 \# 1) 
4.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (範例 \# 3) 
5.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (標記 \# 2) 

在此範例中，資料流程接收在處理範例2之後必須傳送標記1的 [MEStreamSinkMarker](mestreamsinkmarker.md) 事件 \# \# ，並在 \# 處理範例3之後傳送標記2的事件 \# 。

如果用戶端排清資料流程接收，資料流程接收會立即處理佇列中的所有標記。 它會將這些事件的狀態碼設定為 E \_ ABORT。

某些標記包含與媒體接收器相關的資訊：

-   **MFSTREAMSINK \_標記 \_ 刻度**：指出資料流程中有間距。 下一個範例將會是不連續的。
-   **MFSTREAMSINK \_標記 \_ ENDOFSEGMENT**：表示資料流程的區段結尾或結尾。 下一個範例 (是否有任何) 可能是不連續的。
-   **MFSTREAMSINK \_標記 \_ 事件**：包含事件。 根據事件種類和媒體接收器的執行，媒體接收器可能會處理事件或忽略它。

## <a name="state-changes"></a>狀態變更

媒體接收會透過媒體接收器的 [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) 介面，通知呈現時鐘中的狀態變更。 當用戶端設定簡報時鐘時，媒體接收器會呼叫 [**IMFPresentationClock：： AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) ，以註冊來自時鐘的通知。 下表摘要說明媒體接收器回應時鐘狀態變更的行為。



| 時鐘狀態變更                                         | 來樣加工                                                                                                                                                                                                                                             | 標記處理                                                                                                                                                                                   |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | 時間戳記等於或晚于時鐘開始時間的進程範例。                                                                                                                                                                              | 在處理標記之前收到的所有範例都傳送 [MEStreamSinkMarker](mestreamsinkmarker.md) 事件。                                                                 |
| [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause)     | 媒體接收器可能會在暫停時失敗 [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) 。<br/> 如果媒體接收器在暫停時接受樣本，則必須先將它們排在佇列中，直到時鐘重新開機為止。 暫停時，請勿處理任何已排入佇列的範例。<br/> | 如果有已排入佇列的範例，請將標記放在相同的佇列上。 當時鐘重新開機時，傳送標記事件。<br/> 否則，請立即傳送標記事件。<br/>                    |
| [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | 處理在暫停時排入佇列的任何範例，然後將其視為與 [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)相同。                                                                                                                         | 傳送已排入佇列之標記的 [MEStreamSinkMarker](mestreamsinkmarker.md) 事件 (使用範例處理) 進行序列化，然後將相同的視為 [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)。 |
| [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | 捨棄所有已排入佇列的範例。 對 [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) 的後續呼叫可能會失敗。                                                                                                                                                      | 傳送已排入佇列的標記事件。 在後續呼叫 [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)時，立即傳送標記事件。                                                              |



 

此外，當資料流程接收完成狀態轉換時，必須傳送下列事件：

-   [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)， [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart)： [MEStreamSinkStarted](mestreamsinkstarted.md) 事件
-   [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause)： [MEStreamSinkPaused](mestreamsinkpaused.md) 事件
-   [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)： [MEStreamSinkStopped](mestreamsinkstopped.md) 事件

## <a name="finalizing"></a>敲定

在傳遞最後一個範例之後，有些媒體接收器需要額外的處理步驟。 這項需求通常適用于封存接收，必須將標頭或索引寫入至檔案。 如果媒體接收器需要任何最終處理，它會公開 [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) 介面。

用戶端提供最後一個範例之後，用戶端就會查詢這個介面。 如果媒體接收器支援介面，用戶端會呼叫 [**IMFFinalizableMediaSink：： BeginFinalize**](/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize) 來以非同步方式執行最終處理。 這個方法會遵循 [非同步回呼方法](asynchronous-callback-methods.md)中所述的標準媒體基礎非同步模型。 媒體接收器可以假設用戶端會呼叫 **BeginFinalize**。 無法呼叫 **BeginFinalize** 可能會導致檔案撰寫不正確。

## <a name="shutting-down"></a>關閉

當用戶端使用媒體接收器完成時，用戶端會呼叫 [**IMFMediaSink：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown)。 在這個方法內，媒體接收器應該會中斷任何迴圈參考計數。 一般而言，媒體接收和資料流程接收之間會有迴圈參考。

如果您使用事件佇列 helper 物件來執行 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)，請在事件佇列上呼叫 [**IMFMediaEventQueue：： Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) 。 這個方法會關閉事件佇列，並對目前正在等候事件的任何呼叫端發出信號。

關機之後，媒體接收器上的所有方法都會傳回 MF \_ E \_ 關機，但 **IUnknown** 方法除外。

## <a name="media-sink-interfaces"></a>媒體接收器介面

下表列出媒體接收器可透過 **QueryInterface** 公開的標準介面。 媒體接收也可以公開自訂介面。



| 介面                                                      | 描述                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                           | 媒體接收器的主要介面。 (必要項。)                                            |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                 | 用來在簡報時鐘變更狀態時通知媒體接收器。 (必要項。)              |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)     | 如果媒體接收器必須執行最終處理步驟，請執行。 (選擇性。)                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                         | 如果媒體接收器公開任何服務介面，請執行。 (選擇性。)                       |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)       | 如果媒體接收器傳送任何事件，則執行。 (選擇性。)                                     |
| [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)             | 如果媒體接收器支援預先執行，則會執行。 (選擇性。)                                     |
| [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) | 如果媒體接收器可以提供簡報時鐘的時間來源，則會執行。 (選擇性。) |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                   | 如果媒體接收器可以調整播放品質，請執行。 (選擇性。)                          |



 

媒體接收器可以選擇性地將下列介面做為服務來執行。



| 服務介面                        | Description                                    |
|------------------------------------------|------------------------------------------------|
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) | 報告支援播放速率的範圍。 |



 

如需服務介面和 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)的詳細資訊，請參閱 [服務介面](service-interfaces.md)。

## <a name="stream-sink-interfaces"></a>資料流程接收介面

資料流程接收必須透過 **QueryInterface** 公開下列介面。



| 介面                                                | 描述                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)                   | 資料流程接收的主要介面。 (必要項。)                                                      |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | 佇列事件。 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)介面會繼承這個介面。 (必要項。) |



 

目前沒有針對資料流程接收定義任何服務介面。

## <a name="stream-sink-events"></a>資料流程接收事件

下表列出針對一般資料流程接收定義的事件。 資料流程接收也可以傳送此處未列出的自訂事件。



| 事件                                                                  | 描述                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)             | 資料流程接收的媒體類型已不再有效。 (選擇性。) |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                           | 已處理標記。 (必要項。)                          |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                           | 資料流程接收已暫停。 (必要項。)                      |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                     | 預先執行已完成。 (選擇性。)                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                 | 串流接收器已變更播放速率。 (選擇性。)       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)             | 要求新的範例。 (必要項。)                       |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) | 已完成清除要求。 (選擇性。)                   |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                         | 資料流程接收器已啟動。 (必要項。)                     |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                         | 資料流程接收已停止。 (必要項。)                     |



 

目前沒有針對媒體接收器定義一般用途的事件。 某些媒體接收可能會傳送自訂事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎管線](media-foundation-pipeline.md)
</dt> <dt>

[媒體基礎架構](media-foundation-architecture.md)
</dt> </dl>

 

 




