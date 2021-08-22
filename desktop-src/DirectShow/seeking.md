---
description: 尋求
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: 尋求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e087ce981d6548dfeef7ac8d3cb7bc17a69ff952ce95646cd896ace30af941
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951920"
---
# <a name="seeking"></a>尋求

篩選準則支援搜尋 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面。 應用程式會查詢篩選 Graph 管理員以 **IMediaSeeking** ，並使用它來發出搜尋命令。 篩選 Graph 管理員會將每個搜尋命令分散到圖形中的所有轉譯器篩選器。 每個轉譯器都會透過上游篩選的輸出圖釘，將命令傳遞給上游，直到到達可執行搜尋的篩選準則為止。 通常來源篩選器或剖析器篩選器（例如 [AVI 分隔](avi-splitter-filter.md)器）會執行搜尋作業。

當篩選準則執行搜尋作業時，它會清除任何暫止的資料。 結果是將搜尋命令的延遲降至最低，因為現有的資料會從圖表中清除。 在 seek 命令之後，資料流程時間會重設為零。

下圖說明事件的順序。

![事件的順序](images/seeking.png)

如果剖析器篩選器有多個輸出釘選，通常會指定其中一個來接受搜尋命令。 其他 pin 會拒絕或忽略它們所收到的任何搜尋命令。 如此一來，剖析器就會將其所有資料流程保持同步。 不過，所有輸出圖釘都應該執行 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 和 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) ，以傳回篩選準則的搜尋功能。 這可確保篩選 Graph 管理員會將正確的值傳回給應用程式。

篩選器的 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面已被取代。 Automation 用戶端仍然需要在篩選 Graph 管理員上使用此介面，因為 **IMediaSeeking** 不是自動化相容，但是篩選 Graph 管理員會將所有 **IMediaPosition** 呼叫轉譯為 **IMediaSeeking** 呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[沖洗](flushing.md)
</dt> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



