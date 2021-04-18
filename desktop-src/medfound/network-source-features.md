---
description: 網路來源功能
ms.assetid: a4e20ecb-c145-4823-ae59-f6fc88593d86
title: 網路來源功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e937a97cf743740d9cebf84ad477c52cdee5083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562782"
---
# <a name="network-source-features"></a>網路來源功能

網路來源提供串流處理媒體檔案的基底執行，並公開 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面。 特定網路來源的執行取決於用來開啟來源的通訊協定（例如 RTSP 或 HTTP）。 通訊協定特定的網路來源會擴充基本網路功能。 如需支援的配置和通訊協定的相關資訊，請參閱 [支援的通訊協定](supported-protocols.md)。

網路來源：

-   會執行快取、proxy 偵測和自動重新連接等功能。
-   將與來源解析程式通訊協定無關的呼叫轉換為通訊協定特定的呼叫。
-   與通訊端層和作業系統互動。 剖析 SDP 描述並使用它作為設定資料，並從基礎通訊端層讀取串流資料。 接收時，網路來源負責重新排列和要求重新傳輸封包。

## <a name="network-source-creation"></a>建立網路來源

從網路建立來源的媒體來源與本機檔案的媒體來源不同。 應用程式會將來源的 URL 傳遞至 [來源解析程式](source-resolver.md) 方法（例如 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 或 [**IMFSourceResolver：： BEGINCREATEOBJECTFROMURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) ），並指定 MF \_ 解析 \_ MEDIASOURCE 旗標。 如需使用此旗標的詳細資訊，請參閱 [使用來源解析程式](using-the-source-resolver.md)。

來源解析程式會根據應用程式所提供的配置，載入適當的配置處理常式物件，此物件會公開 [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) 介面。 應用程式也可以藉由呼叫 [**IMFSchemeHandler：： BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)，直接使用配置處理常式來建立網路來源。

如需詳細資訊，請參閱 [配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)。

媒體基礎不支援網路來源的位元組資料流程。 只有下載的內容案例才支援位元組資料流程物件。 所有資料都會儘快傳輸，以便在本機電腦上儲存為檔案。 web 伺服器提供下載的資料。 下載開始之後，就不會從用戶端到伺服器之間進行通訊。 在此情況下，會使用 HTTP 下載通訊協定。

如果應用程式要求來源解析程式為 "HTTP："、"mms：" 或 "rtsp：" 配置建立位元組資料流程物件，則呼叫會失敗，並出現 MF \_ E \_ 不支援的 \_ 配置錯誤。

> [!Note]  
> 在 Windows 7 中，網路來源支援 Windows Media 站檔案 (。.NSC) 。 這些檔案是用來透過網路進行媒體內容的多播串流處理。 為指定的建立網路來源。.NSC 檔，應用程式必須使用來源解析程式。

 

如果應用程式使用配置處理常式，則非同步呼叫會忽略 *dwFlags* 參數，並在完成時傳回網路來源的指標。

下圖顯示使用網路來源進行媒體串流處理的資料流程。

![流程圖，顯示從應用程式到串流伺服器的路徑，以及網路來源與媒體會話之間的迴圈](images/3f9186ea-53ed-4a31-a097-92f39fa08624.gif)

## <a name="network-source-configuration"></a>網路來源設定

本主題說明網路來源所支援的功能，以及相關聯的設定選項。 應用程式可以在建立網路來源物件時設定網路來源。 這些選項會儲存在 **IPropertyStore** 物件中，應用程式必須在來源解析程式方法的 *pProps* 參數中傳遞，或 [**IMFSchemeHandler：： BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)。

### <a name="auto-reconnect"></a>自動重新連線

網路來源的自動重新連線功能可讓用戶端在伺服器的 TCP 連線失敗或用戶端無法接收封包時，自動重新連線至媒體伺服器。 連接失敗時，網路來源會使用先前連線中使用的相同設定，嘗試重新連線至媒體伺服器。 重新連接程式是非同步。 當重新連線時，網路來源會引發 [MEReconnectStart](mereconnectstart.md) 事件，而當重新連線成功或失敗時，則會引發 [MEReconnectEnd](mereconnectend.md) 事件。

如果重新連接嘗試次數超過 [**MFNETSOURCE \_ AUTORECONNECTLIMIT**](mfnetsource-autoreconnectlimit-property.md) 屬性所指定的最大值，則重新連接作業將會取消。 重新連接嘗試次數會儲存在 [**MFNETSOURCE \_ AUTORECONNECTPROGRESS**](mfnetsource-autoreconnectprogress-property.md) 屬性中。

自動重新連線可讓媒體內容順暢地播放，即使連至媒體伺服器的 TCP 連線失敗也一樣。 若要順利播放，用戶端的快取中必須有足夠的資料（至少1到2分鐘），才能繼續播放，直到重新連接為止。 可以在 [**MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md) 屬性中設定網路來源可以緩衝的最大資料量。

### <a name="fast-streaming"></a>快速串流處理 

網路來源用戶端要求伺服器以較快的速率來串流內容開頭的一些資料，而不是由內容位元速率所指定。 如果伺服器上已啟用 [ *快速啟動* ]，伺服器會傳送加速的位元速率串流，讓用戶端可以更快緩衝足夠的資料量，而非即時。 這可透過將初始緩衝延遲降至最低，進而改善使用者體驗，這可能是因為用戶端電腦或網路的低速度，以及可用的頻寬等各種因素所致。

若要指定用戶端可以要求的快速串流資料量，請設定 [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) 屬性。 如果網路來源使用 UDP 做為傳輸通訊協定，請改為設定 [**MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION**](mfnetsource-maxudpacceleratedstreamingduration-property.md) 屬性，以指定最大的快速串流資料量。

您也可以透過 *快速快* 取功能，在用戶端上進行快速串流，以比即時串流隨選內容更快，並在用戶端的本機快取上快取資料。 若要使用這種類型的快速串流，必須在網路來源上啟用快速快取，且伺服器必須支援。 當用戶端從伺服器要求內容時，網路來源會先檢查內容是否已在用戶端的快取中。 如果內容位於用戶端的本機快取中，而且尚未過期，則會轉譯。 如果內容不在本機快取中或已過期，則會串流處理和快取內容，而且網路來源會從本機快取中播放。 在後續的要求中，針對播放清單，只會快取遺漏的專案，然後再播放。 如果播放清單專案已在用戶端的本機快取中，則會從該處播放，而不會再次快取。

依預設，網路來源用戶端上會啟用快速快取。 但是，下列因素也會決定是否要使用此功能：

-   用戶端必須有額外的頻寬可供下載，且快取內容的速度比一般速度還要快。
-   用戶端必須有足夠的磁碟空間。 如果用戶端在快取要求的隨選內容之後，有小於 100 MB 的可用磁碟空間，則不會進行快取，但會同時進行資料流程處理和轉譯。

快取功能是由 [**MFNETSOURCE \_ CACHEENABLED**](mfnetsource-cacheenabled-property.md) 屬性所控制。

### <a name="buffer-management"></a>緩衝區管理

網路來源提供有效率的緩衝區管理，可監視用戶端上的緩衝區狀態。 根據預設，網路來源會在啟動時緩衝5秒的資料。 您可以藉由設定 [**MFNETSOURCE \_ BUFFERINGTIME**](mfnetsource-bufferingtime-property.md) 屬性來設定這個值。 根據此屬性值，網路來源會計算足夠的緩衝區大小，以確保媒體內容的播放流暢且不中斷。 如果這個屬性設定為0，則會停用緩衝區管理。 當緩衝區中的內容數量很低時，網路來源會開始緩衝並引發 [MEBufferingStarted](mebufferingstarted.md) 事件，以指出已開始緩衝。 收到此事件時，管線會停止轉譯。 當緩衝處理完成時，網路來源會引發 [MEBufferingStopped](mebufferingstopped.md) 事件，而用戶端可以再次開始轉譯。

用戶端會在累積了第一個樣本的緩衝區大小所指出的資料量之後，開始轉譯內容。 如果這個值低於計算的緩衝區大小，則會立即開始播放。 此行為非常類似于快速啟動功能。

[**MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md)屬性會儲存可以緩衝的最大資料量。

### <a name="bandwidth-selection"></a>頻寬選取

當用戶端連線至媒體伺服器時，在連線設定過程中，網路來源會執行 *靜態封包配對* 測量，以估計用戶端與伺服器之間的初始連結頻寬。 根據此測量結果，用戶端可以選取符合估計頻寬的音訊和影片串流。 這可確保流暢地播放串流媒體內容。

在快速啟動階段期間，會執行 *動態封包配對* 度量。 在此程式中，用戶端會收到大量的資料，也就是多個封包或範例。

動態封包組量測的結果比靜態封包配對測量傳回的連結頻寬估計更為精確，因為靜態封包組進程會傳送固定大小的單一封包，這可能不會產生高頻寬網路的精確結果。

應用程式可以使用 [**MFNETSOURCE \_ PPBANDWIDTH**](mfnetsource-ppbandwidth-property.md) 屬性來取得估計的頻寬。

網路狀況可能會動態變更，導致網路來源的播放發生問題。 網路來源可以根據接收速率和緩衝區狀態變更用戶端的初始資料流程選取專案。 例如，用戶端可能會在網路擁塞期間切換至較低的位元速率，並在網路流量改善時切換回較高的位元速率，且用戶端已累積足夠的緩衝內容數量。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 



