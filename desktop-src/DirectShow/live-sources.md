---
description: 即時來源
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: 即時來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43486cf3db797f493c9446bf782989b8beaae829
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467699"
---
# <a name="live-sources"></a>即時來源

即時來源也稱為 *推送來源*，會即時接收資料。 範例包括影片捕獲和網路廣播。 一般情況下，即時來源無法控制資料抵達的速率。

如果下列任一條件成立，則會將篩選視為即時來源：

-   篩選準則 \_ \_ \_ \_ 會 \_ 從 [**IAMFILTERMISCFLAGS：： GetMiscFlags**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) 方法傳回 AM 篩選其他旗標為來源旗標，且至少其中一個輸出圖釘會公開 [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) 介面。
-   此篩選器會公開 [**IKsPropertySet**](ikspropertyset.md) 介面，並有 (釘選 \_ 類別 \_ 捕獲) 的捕獲 pin。 如需詳細資訊，請參閱 [釘選屬性集](pin-property-set.md) 。

如果即時來源篩選器提供時鐘，則篩選圖形管理員會偏好在選擇 Graph 參考時鐘時使用時鐘。 如需詳細資訊，請參閱 [參考時鐘](reference-clocks.md) 。

**延遲**

篩選器的延遲是篩選器處理範例所需的時間量。 針對即時來源，延遲是由用來保存範例的緩衝區大小所決定。 例如，假設篩選圖形的影片來源的延遲為33毫秒 (ms) ，而音訊來源的延遲為500毫秒。 在比對音訊範例到達音訊轉譯器之前，每個影片框架都會抵達影片轉譯器大約470毫秒。 除非圖形針對差異進行補償，否則音訊和影片將不會同步處理。

即時來源可以透過 [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) 介面進行同步處理。 除非應用程式藉由呼叫 [**IAMGraphStreams：： SyncUsingStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) 方法來啟用同步處理，否則篩選圖形管理員不會同步處理即時來源。 如果同步處理已啟用，則篩選圖形管理員會查詢每個來源篩選以進行 **IAMPushSource**。 如果篩選準則支援 **IAMPushSource**，則篩選圖形管理員會呼叫 [**IAMLatency：： GetLatency**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) 來取得篩選準則的預期延遲。 **IAMPushSource** 介面 (繼承 [**IAMLatency**](/windows/desktop/api/Strmif/nn-strmif-iamlatency)) 。從結合的延遲值，篩選圖形管理員會決定圖形中預期的最大延遲。 然後，它會呼叫 [**IAMPushSource：： SetStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) 來提供每個來源篩選一個資料流程位移，該篩選會將它新增至它所產生的時間戳記。

這個方法主要是供即時預覽之用。 不過，請注意，即時捕獲裝置上的預覽 pin (例如相機) 不會在其所提供的範例上設定時間戳記。 因此，若要將此方法與 live capture 裝置搭配使用，您必須從 capture pin 進行預覽。 如需詳細資訊，請參閱 [DirectShow 影片捕獲篩選](directshow-video-capture-filters.md)。

[VFW Capture](vfw-capture-filter.md)篩選器和 [音訊捕獲](audio-capture-filter.md)篩選器目前支援 [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource)介面。

**速率比對**

如果轉譯器篩選使用一個參考時鐘來排程範例，但來源篩選器使用不同的時鐘來產生這些樣本，則可能會在播放時發生問題。 轉譯器的執行速度可能會比來源還快，導致資料中的間距。 或者，它的執行速度可能會比來源還慢，導致範例「變大」，直到某個時間點，圖形才會捨棄範例。 一般情況下，即時來源無法控制其生產費率，因此轉譯器應該會比對來源的速率。

目前，只有音訊轉譯器會執行速率比對，因為音訊播放的問題比影片中的問題更明顯。 若要執行比對，音訊轉譯器必須選取它將符合的速率。 它會使用下列演算法：

-   如果圖形未使用參考時鐘，則音訊轉譯器不會嘗試比對速率。  (，只要圖形沒有參考時鐘，則會在其抵達時立即轉譯樣本。 ) 
-   否則，如果圖形有參考時鐘，則音訊轉譯器會使用先前所述的準則來檢查是否有即時來源上游。 如果不是，則音訊轉譯器不符合費率。
-   如果有即時來源上游，且該來源在其輸出 pin 上公開 [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) 介面，則音訊轉譯器會呼叫 [**IAMPushSource：： GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags)。 它會尋找下列其中一個旗標：
    -   \_PUSHSOURCECAPS \_ 內部 \_ RM。 此旗標表示來源篩選器有自己的速率比對機制，因此音訊轉譯器不符合費率。
    -   AM \_ PUSHSOURCECAPS \_ 無法 \_ 上線。 此旗標表示來源篩選不是真正的即時來源，即使它會公開 [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) 介面也一樣。 因此，音訊轉譯器不符合費率。
    -   \_PUSHSOURCECAPS \_ 私用 \_ 時鐘。 此旗標表示來源篩選器會使用私用時鐘來產生時間戳記。 在此情況下，音訊轉譯器會與時間戳記的速率相符。  (如果樣本沒有時間戳記，則轉譯器會忽略此旗標。 ) 
-   如果 [**GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) 未 (零) 傳回任何旗標，音訊轉譯器的行為取決於圖形時鐘，以及範例是否有時間戳記：
    -   如果音訊轉譯器不是圖形時鐘，而且樣本具有時間戳記，則音訊轉譯器會比對時間戳記的速率。
    -   如果範例沒有時間戳記，音訊轉譯器會嘗試符合傳入音訊資料的速率。
    -   如果音訊轉譯器是圖形時鐘，則會嘗試比對傳入的資料速率。

最後一個案例的原因如下：如果音訊轉譯器是參考時鐘，而來源篩選器使用相同的時鐘來產生時間戳記，則音訊轉譯器無法比對時間戳記的速率。 如果有的話，則會嘗試比對速率與本身，這可能會導致時鐘漂移。 因此，在此情況下，轉譯器會符合傳入音訊資料的速率。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



