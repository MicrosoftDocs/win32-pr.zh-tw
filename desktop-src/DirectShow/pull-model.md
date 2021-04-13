---
description: 提取模型
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: 提取模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509997"
---
# <a name="pull-model"></a>提取模型

在 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面中，上游篩選器會決定要傳送的資料，並將資料推送至下游篩選。 針對某些篩選， *提取* 模型更適合。 在這裡，下游篩選器會向上游篩選要求資料。 範例仍會從輸出釘選到輸入釘選，但下游篩選器會起始資料流程。 這種類型的連接會使用 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面。

提取模型的一般用途是在檔案播放中。 例如，在 AVI 播放圖形中，非同步檔案 [來源](file-source--async--filter.md) 篩選會執行一般檔案讀取作業，並將資料傳遞為位元組資料流程，且沒有格式資訊。 [Avi 分隔](avi-splitter-filter.md)器篩選器會讀取 AVI 標頭，並將資料流程剖析成影片和音訊範例。 AVI 分隔器可判斷所需的資料比非同步檔案來源篩選更好，因此它會使用 **IAsyncReader** 而不是 **IMemInputPin**。

若要從輸出圖釘要求資料，輸入的 pin 會呼叫下列其中一種方法：

-   [**IAsyncReader：： Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader：： SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)。

第一個方法是非同步，可支援多個重迭讀取。 其他則為同步。

理論上，任何篩選都可以支援 **IAsyncReader**，但實際上它是針對連接到剖析器篩選器的來源篩選所設計。 剖析器的運作方式非常類似于推播模型中的來源篩選。 當它暫停時，它會建立串流執行緒，從 **IAsyncReader** 連接提取資料並將其推送至下游。 輸出圖釘會使用 **IMemInputPin**，而圖形的其餘部分會使用標準推送模型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選圖形中的資料流程](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



