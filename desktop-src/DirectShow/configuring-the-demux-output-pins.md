---
description: 設定 Demux 輸出圖釘
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: 設定 Demux 輸出圖釘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56a24af3f49f26efe4ff6afad075a3cef61fcd1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109416"
---
# <a name="configuring-the-demux-output-pins"></a>設定 Demux 輸出圖釘

當 MPEG-2 demux 收到資料的封包時，它必須判斷哪個輸出圖釘應該剖析和傳遞資料。 在程式資料流程模式中，demux 會將串流識別碼對應至輸出圖釘。 在傳輸資料流程模式中，它會將 Pid 對應到輸出圖釘。 例如，在傳輸資料流程模式中，如果 PID 0x31 對應至 pin 0，則每個具有該 PID 編號的 TS 封包都會路由傳送至輸出 pin 0。 如果 demux 收到的封包的資料流程識別碼或 PID 未對應到任何輸出釘選，則只會捨棄封包。

在提取模式中，demux 會自動在檔案中建立音訊和影片串流的輸出圖釘，並將串流識別碼對應至圖釘。

在推送模式中，輸出圖釘必須由應用程式或其他篩選器設定。 針對使用廣播驅動程式架構 (BDA) 的數位電視來源，網路提供者篩選器會使用 .TIF 篩選器來設定 demux。 應用程式不需要執行任何動作。 在其他情況下，應用程式必須設定輸出圖釘。

Demux 的開頭不是輸出圖釘。 若要建立輸出釘選，請在篩選準則上呼叫 [**IMpeg2Demultiplexer：： CreateOutputPin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) 方法。 這個方法會採用媒體類型和 pin 名稱，並傳回 **IPin** 指標。 當 pin 連線到另一個篩選（通常是一個解碼器）時，就會使用該媒體類型，例如，將 [Demux 與基本資料流程搭配使用](using-the-demux-with-elementary-streams.md)的區段。 Pin 名稱可以是任何您喜歡的名稱，但不允許重複的 pin 名稱。

接下來，將一個或多個串流識別碼或 Pid 指派給新的輸出 pin。 針對程式資料流程，查詢 **IMPEG2StreamIdMap** 的 pin，然後呼叫 [**IMPEG2StreamIdMap：： MapStreamId**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid)。 針對傳輸資料流程，查詢 **IMPEG2PIDMap** 的 pin，然後呼叫 [**IMPEG2PIDMap：： MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid)。

Demux 可以剖析 TS 封包的方式有好幾種。 針對每個輸出圖釘，剖析方法是由 **MapPID** 方法的 *MediaSampleContent* 參數所決定。



| 值                     | 描述                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 媒體 \_ 基本 \_ 資料流程 | 篩選準則會傳遞 PE 承載。 在此模式中，篩選準則會 depacketizes PE 封包，因此下游篩選器會接收 ES 位元組資料流程，而不含 PE 封包標頭。 僅 (音訊和影片串流。 )                                                                                                                                                      |
| 媒體 \_ MPEG2 \_ PSI         | 篩選會提供完整的 PSI 區段，例如 PAT 資料表、PMT 資料表、貓資料表等等。                                                                                                                                                                                                                                                               |
| 媒體 \_ 傳輸 \_ 承載 | 篩選會從 TS 封包中解壓縮承載，並傳遞它們，而不需要進一步剖析。 針對基本資料流程，這表示 demux 會提供整個 PE 封包，包括 PE 封包標頭。                                                                                                                                                    |
| 媒體 \_ 傳輸封 \_ 包  | 篩選會提供整個 TS 封包。 Demux 會根據其 Pid 路由傳送 TS 封包，但不會檢查或處理封包。 具有錯誤的封包不會被篩選掉。Demux 不會重新多工傳遞封包，而且產生的輸出資料流程不是相容的 MPEG-2 傳輸串流。 這個 *模式稱為通過模式。* |



 

對於程式資料流程，demux 一律會傳遞 PE 承載。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MPEG-2 信號信號](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



