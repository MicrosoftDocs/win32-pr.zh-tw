---
description: Sequencer 來源事件
ms.assetid: 28654bae-9ce2-467b-b769-63279d69b173
title: Sequencer 來源事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf97cc5ff25c8a5fc40fa4990bf38c652f94e63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974567"
---
# <a name="sequencer-source-events"></a>Sequencer 來源事件

當 [Sequencer 來源](sequencer-source.md) 播放一系列的檔案時，媒體會話通常會傳送正常播放期間傳送的相同事件，以及 [媒體會話事件](media-session-events.md)中所列出的事件。 應用程式會使用媒體會話的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面取得這些事件。

此外，還有一些特定于播放清單區段的事件。



| 事件                                                                                                   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MENewPresentation](menewpresentation.md)                                                              | 通知應用程式要預先進行下一個拓撲。<br/> 為了在兩個連續的簡報之間提供順暢的轉換，sequencer 來源會事先載入下一個拓撲。 當使用中拓撲仍在播放時，sequencer 來源會傳送此事件以供下一個拓撲，只要來源中有可用的後續拓撲即可。<br/> 此事件的事件資料是下一個拓撲的表示描述項。 應用程式會負責在媒體會話上設定對應的拓撲，如 [使用 Sequencer 來源](using-the-sequencer-source.md)中所述。<br/> |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                            | 當媒體會話完成播放目前的區段時，如果該區段後面接著另一個區段，sequencer 來源就會引發此事件。  (如果目前區段是最後一個區段，sequencer 來源會改為引發 [MEEndOfPresentation](meendofpresentation.md) 事件。 ) <br/> 媒體會話將此事件轉送到應用程式。 一般來說，當媒體會話開始處理下一個區段之後，應用程式會收到 [MEEndOfPresentationSegment](meendofpresentationsegment.md) ，但是媒體接收器仍會提供上一個區段的範例。<br/>                            |
| [MESessionTopologyStatus](mesessiontopologystatus.md)，狀態為 **MF \_ TOPOSTATUS \_ 接收已 \_ 切換**。 | 當媒體會話轉換到 sequencer 來源中的下一個拓撲，而媒體接收器已完成播放先前的拓撲時，就會引發此事件。 此事件包含下一個拓撲的指標。                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="example-1-playback-without-skipping"></a>範例1：不略過的播放

牽涉到 sequencer 來源時，從媒體會話取得的事件數目可能會造成混淆，尤其是因為與某個區段相關聯的事件通常會與下一個區段的事件交錯。

在第一個範例中，應用程式會將三個區段（S1、S2 和 S3）排入佇列。 第三個區段具有 **SequencerTopologyFlags \_ 最後一個** 旗標，表示其為序列中的最後一個區段。 每個事件對應的區段都是以括弧括住。 也會列出應用程式的 [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 呼叫，讓作業的順序更清楚。

-   應用程式呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1) 
-   [MESessionTopologySet](mesessiontopologyset.md) (S1) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ READY** (S1) 
-   [MENewPresentation](menewpresentation.md) (S2 預先) 
-   應用程式呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 啟動 \_ 來源** (S1) 的起點
-   [MESessionTopologySet](mesessiontopologyset.md) (S2) 
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S1) 的結尾
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_** (S1) 結束
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 接收 \_ 切換** (轉換至 S2) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ READY** (S2) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 啟動 \_ 來源** (開始 S2) 
-   [MENewPresentation](menewpresentation.md) (S3 預先) 
-   應用程式呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2) 
-   [MESessionTopologySet](mesessiontopologyset.md) (S3) 
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S2) 的結尾
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 結束** (S2) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 接收 \_ 切換** (轉換至 S3) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ READY** (S3) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 啟動 \_ 來源** (S3) 起點
-   [MEEndOfPresentation](meendofpresentation.md) (S3 結尾;最後一個區段) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 結束**
-   [MESessionEnded](mesessionended.md)

這份清單不包含您可能會收到的每個事件。  (例如，它會省略 [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) 事件，每當會話功能變更時就會傳送此事件。 應用程式通常會在簡報中收到多個 MESessionCapabilitiesChanged 事件。 ) 此處所列的事件是顯示從一個區段轉換到下一個區段的事件。 最重要的事件是 [MENewPresentation](menewpresentation.md)，它會指示應用程式預先進行下一個拓撲，並使用 [MEEndOfPresentationSegment](meendofpresentationsegment.md)來表示區段結尾 (除了最後一個區段) 之外。

由於媒體基礎中的事件是非同步，而且不會使用方法呼叫進行序列化，因此確切的順序可能會不同。 例如，您可以在應用程式呼叫 [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) for S2 之前，接收 S1 的 **MF \_ TOPOSTATUS \_ 已啟動 \_ 來源**。

此外，您可能無法取得此處所列的每個事件。 例如，除非最後一個區段具有 **SequencerTopologyFlags 的 \_ 最後一個** 旗標，否則不會傳送 [MEEndOfPresentation](meendofpresentation.md)和 [MESessionEnded](mesessionended.md)事件。

最後，這份清單並不表示時間。 從「開始 S1」到「S1 結尾」的時間是 S1 的整個持續時間，這可能是幾秒鐘或數小時，視來源而定。

## <a name="example-2-playback-with-segment-skipping"></a>範例2：使用區段略過播放

在此範例中，應用程式會將相同的區段排入佇列，但在播放區段1時跳到區段3。 在此情況下，會傳送下列事件：

-   應用程式呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S1) 
-   [MESessionTopologySet](mesessiontopologyset.md) (S1) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ READY** (S1) 
-   [MENewPresentation](menewpresentation.md) (S2 預先) 
-   應用程式呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S2) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 啟動 \_ 來源** (S1) 的起點
-   [MESessionTopologySet](mesessiontopologyset.md) (S2) 
-   應用程式呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) (跳至 S3) 
-   [MENewPresentation](menewpresentation.md) (S3 預先) 
-   應用程式呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) (S3) 
-   [MESessionStarted](mesessionstarted.md)
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S1 已取消) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_** (S1) 結束
-   [MESessionTopologySet](mesessiontopologyset.md) (S3) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 接收 \_ 切換** (轉換至 S2) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ READY** (S2) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 已啟動 \_ 來源** (S2) 
-   [MEEndOfPresentationSegment](meendofpresentationsegment.md) (S2 已取消) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 結束** (S2) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 接收 \_ 切換** (轉換至 S3) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **TOPOSTATUS \_ READY** (S3) 
-   [MESessionTopologyStatus](mesessiontopologystatus.md)： **MF \_ TOPOSTATUS \_ 已啟動 \_ 來源** (S3) 

當應用程式呼叫 [**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 跳到區段3時，sequencer 來源會取消區段1（仍在播放）。 此區段的 [MEEndOfPresentationSegment](meendofpresentationsegment.md) 事件包含 [ [**MF \_ 事件 \_ 來源 \_ 拓撲 \_ 已取消**](mf-event-source-topology-canceled-attribute.md) ] 屬性，表示區段因為已取消而結束。 然後，由於區段2已經預先匯總，因此會啟動該區段，但是會立即取消。 區段2的 MEEndOfPresentationSegment 事件也包含 **MF \_ 事件 \_ 來源 \_ 拓撲 \_ 取消** 屬性。 然後，會話可以切換到區段3並正常播放。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Sequencer 來源](about-the-sequencer-source.md)
</dt> <dt>

[Sequencer 來源](sequencer-source.md)
</dt> </dl>

 

 




