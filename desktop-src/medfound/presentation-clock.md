---
description: 簡報時鐘
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: 簡報時鐘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0219b6384373fd75bc8a424935e502841071f69eaa9ae719ec6ed35c950218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239155"
---
# <a name="presentation-clock"></a>簡報時鐘

*簡報時鐘* 是一個物件，它會產生簡報的時鐘時間。 標記法所報告的時間稱為 *呈現時間*。 簡報中的所有資料流程都會與展示時間同步處理。 簡報時鐘會公開下列介面。



| 介面                                            | 描述                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | 使用呈現時鐘的主要介面。 |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | 控制時脈速率。                            |
| [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | 提供計時器回呼。                          |
| [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | 關閉呈現時鐘。                  |



 

媒體接收器會使用呈現時間來排程轉譯樣本的時機。 每當媒體接收器收到新的範例時，它會從範例取得時間戳記，並在指定的時間轉譯樣本，或盡可能接近該時間。 由於拓撲中的所有媒體接收器都會共用相同的呈現時鐘，因此會同步處理多個串流 (例如音訊和影片) 。 媒體來源和轉換不會使用簡報時鐘，因為它們不會排定何時提供範例。 相反地，當管線要求新的範例時，它們會產生範例。

如果您使用媒體會話來播放，媒體會話會處理建立簡報時鐘、選取時間來源，以及通知媒體接收器的所有詳細資料。 您的應用程式可能會使用簡報時鐘來取得播放期間目前的呈現時間，否則不會對簡報時鐘呼叫任何方法。

## <a name="clock-time-and-clock-states"></a>時鐘時間和時鐘狀態

若要從呈現時鐘取得最新的時鐘時間，請呼叫 [**IMFPresentationClock：： GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime)。 時鐘時間一律為 100-毫微秒的單位，因此一秒為 10000000 (10 ^ 7) 刻度。 這會對應至 10 MHz 的頻率。

簡報時鐘有三種狀態： [執行中]、[已暫停] 和 [已停止]。

-   若要執行時鐘，請呼叫 [**IMFPresentationClock：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start)。 **Start** 方法會指定時鐘的開始時間。 當時鐘正在執行時，時鐘時間會以目前的時脈速率從開始時間遞增。
-   若要暫停時鐘，請呼叫 [**IMFPresentationClock：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause)。 當時鐘暫停時，不會前進時鐘時間，而 [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) 會傳回時鐘暫停的時間。
-   若要停止時鐘，請呼叫 [**IMFPresentationClock：： stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop)。 當時鐘停止時，時鐘時間不會前進， [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) 會傳回零。

根據預設，時鐘會以1.0 的速率前進，這表示每100納秒1次滴答。 若要變更時鐘前進的速率，請查詢 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面的呈現時鐘，然後呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)。

物件可以接收狀態變更的通知， (包括呈現時鐘) 的速率變更。 若要接收通知，請執行 [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) 介面，並在簡報時鐘上呼叫 [**IMFPresentationClock：： AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) 。 在關機之前，請呼叫 [**IMFPresentationClock：： RemoveClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) 來取消註冊物件。 媒體接收器會使用此機制來接收來自時鐘的通知。

## <a name="presentation-times"></a>展示時間

媒體接收器會嘗試排程每個範例，以便在正確的時間轉譯範例，或盡可能接近正確的時間。 下列定義適用：

-   *簡報時間。* 應呈現樣本的時間。 時間是以100毫微秒為單位來提供。
-   *媒體時間。* 相對於開始內容的時間。 例如，如果影片檔案的長度為10秒，則整個檔案的點半形會有5秒的媒體時間。
-   *時間戳記。* 媒體範例上標記的時間。 若要取得時間戳記，請呼叫 [**IMFSample：： GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime)。 當媒體來源產生範例時，它會設定等於媒體時間的時間戳記。 媒體會話會將時間戳記轉譯為呈現時間。

依預設，媒體時間和表示時間都相同; 例如，如果影片框架在原始程式檔中出現5秒，則媒體時間和呈現時間都是5秒。 如果您使用 [Sequencer 來源](sequencer-source.md)，計時模型會稍微複雜一點，以在區段之間啟用平滑轉換。 如需有關 sequencer 來源時間模型的詳細資訊，請參閱 [順序呈現時間](sequence-presentation-times.md)。

媒體來源一律會設定等於媒體時間的時間戳記。 如果簡報時間與媒體時間不一致，則媒體會話會轉換媒體範例上的時間戳記。 接收到範例時，範例的時間戳記已轉換為展示時間。 接收會根據簡報時鐘的目前時間來排定範例。  (Rateless 接收是例外狀況，因為它們會忽略呈現時鐘。 ) 

如果應用程式搜尋到新位置，媒體會話就會在指定的搜尋時間重新開機表示時鐘。 例如，如果應用程式搜尋檔案中的5秒位置，媒體會話就會在5秒內啟動時鐘。 如果搜尋時間不是落在主要畫面格界限上，媒體來源可能會以稍早的時間戳記來傳遞範例。 這是必要的，如此一來，這些解碼器才能將所有框架解碼。 媒體會話會在達到媒體接收器之前卸載或修剪範例，以便符合要求的搜尋時間。 例如，如果搜尋時間為5秒，則第一個音訊樣本可能會在4.5 秒內啟動。 媒體會話將會從第一個解碼的音訊範例修剪前0.5 秒。

## <a name="creating-the-presentation-clock"></a>建立簡報時鐘

若要建立簡報時鐘，請呼叫 [**MFCreatePresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock)。 若要關閉時鐘，請查詢 [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) 介面，然後呼叫 [**IMFShutdown：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown)。 **MFCreatePresentationClock** 的呼叫端負責呼叫 **Shutdown**;在大部分的情況下，這是媒體會話，而不是應用程式。

## <a name="presentation-time-sources"></a>展示時間來源

無論其名稱為何，簡報時鐘其實不會實際執行時鐘。 相反地，它會從另一個物件（稱為 *展示時間來源*）取得時鐘時間。 時間來源可以是任何會產生正確時鐘刻度的物件，並公開 [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) 介面。 下圖顯示這項程序。

![顯示呈現時鐘與展示時間來源之間關聯性的圖表](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

首次建立簡報時鐘時，不會有時間來源。 若要設定時間來源，請呼叫 [**IMFPresentationClock：： SetTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) ，並提供時間來源 [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) 介面的指標。 時間來源支援與呈現時鐘相同的狀態 (執行中、已暫停和停止) ，而且必須執行 [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) 介面。 簡報時鐘使用此介面來通知時間來源何時變更狀態。 如此一來，時間來源就會提供時鐘刻度，但標記法會起始時鐘的狀態變更。

有些媒體接收器可以存取精確的時鐘，因此會公開 [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) 介面。 尤其是，音訊轉譯器可以使用音效卡的頻率作為時鐘。 在音訊播放中，音訊轉譯器可作為時間來源，讓影片同步到音訊播放速率。 這通常會比嘗試將音訊與外部時鐘比對，產生更好的結果。

媒體基礎也會根據系統時鐘提供展示時間來源。 若要建立這個物件，請呼叫 [**MFCreateSystemTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource)。 當沒有任何媒體接收提供時間來源時，可以使用系統時間來源。

一般情況下，媒體接收器必須使用提供給它的簡報時鐘，無論呈現時鐘使用的時間來源為何。 即使在媒體接收器執行 [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource)時，也適用此規則。 如果簡報時鐘使用其他時間來源，則媒體接收器必須在該時間來源之後，而不是它自己的內部時鐘。

在兩種情況下，媒體接收器不會遵循簡報時鐘：

-   有些媒體接收器 *rateless*。 如果媒體接收器 rateless，它會儘快取用樣本，而不會根據簡報時鐘進行排程。 一般而言，rateless 接收會將資料寫入檔案，因此最好儘快完成此作業。 Rateless 接收會傳回 \_ [**IMFMediaSink：： GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) 方法中的 MEDIASINK rateless 旗標。 當拓撲中的所有接收器都 rateless 時，媒體會話會儘快將資料推送至管線。

-   有些媒體接收無法比對費率與本身的時間來源。 如果是，則接收會傳回 MEDIASINK，而 \_ \_ \_ 其 [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) 方法中的時鐘旗標不能相符。 管線仍可以使用另一個時間來源，但結果將會小於最佳。 接收可能會落後並在播放期間造成問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> </dl>

 

 



