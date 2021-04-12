---
description: MPEG-2 Demux Run-Time 模式
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: MPEG-2 Demux Run-Time 模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109645"
---
# <a name="mpeg-2-demux-run-time-modes"></a>MPEG-2 Demux Run-Time 模式

[Mpeg-2 信號](mpeg-2-demultiplexer.md) ( "demux" ) 可以在 push 模式或 pull 模式下運作。 在推送模式中，資料來自即時來源，例如網路廣播。 在提取模式中，資料來自本機檔案。

-   在 Windows XP 和更新版本中，提取模式僅適用于程式串流。 在舊版平臺上，使用 [Mpeg-2 分隔](mpeg-2-splitter.md) 器篩選器。
-   推送模式適用于所有平臺，適用于程式資料流程和傳輸串流。

因此，demux 支援三種可能的模式：提取模式的程式資料流程、推入模式中的程式資料流程，以及推送模式的傳輸資料流程。 Demux 會決定在執行時間使用的模式。 當輸入連接或第一個輸出 pin 已設定時（以先發生者為准），會決定模式：

-   當輸入 pin 連接：在 Windows XP 和更新版本上，demux 會查詢 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的上游篩選;如果上游篩選器公開該介面，demux 會在提取模式中為程式資料流程設定本身。 否則，demux 會使用 push 模式，而媒體類型會判斷 (程式資料流程或傳輸資料流程) 的資料流程類型。 如需輸入類型清單，請參閱 [**Mpeg-2 信號的媒體類型**](mpeg-2-demultiplexer-media-types.md) 。
-   當第一個輸出 pin 設定時：如果您建立輸出釘選並查詢它以進行 [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap)，demux 會為推送模式中的傳輸資料流程設定本身。 如果您查詢 [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap)的 pin，demux 會為程式資料流程設定本身，也會在推送模式中設定。 針對其他介面進行的任何後續查詢都會失敗，因為 demux 無法一次以兩種模式運作。

一旦 demux 為特定模式設定本身，它就會維持在該模式中。 若要使用不同的模式，您必須建立 demux 的新實例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MPEG-2 信號信號](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



