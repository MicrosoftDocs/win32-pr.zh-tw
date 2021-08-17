---
description: Pin 連接
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Pin 連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfcd407e785e15f4243f3113a63569f8b4b84de517cdde0f63a88eaef79f85c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432288"
---
# <a name="pin-connections"></a>Pin 連接

篩選器會透過 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面，在其針腳上連接。 輸出連接會連線至輸入圖釘。 每個 pin 連線都有媒體類型，由 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構所描述。

應用程式會藉由在篩選 Graph 管理員上呼叫方法來連接篩選，而不會藉由呼叫篩選或釘選上的方法。 應用程式可以藉由呼叫 [**IFilterGraph：： ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect)或 [**IGraphBuilder：：連線**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)方法，直接指定要連接的篩選;或者，它可以使用圖表建立方法（例如 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)）間接連接篩選。

若要讓連接成功，這兩個篩選準則必須在篩選圖形中。 應用程式可以藉由呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法，將篩選新增至圖形。 篩選 Graph 管理員也可以將篩選新增至圖形。 加入篩選準則時，篩選 Graph 管理員會呼叫篩選準則的 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph)方法來通知篩選。

連接程式的一般大綱如下所示：

1.  篩選 Graph 管理員會在輸出釘選上呼叫 [**IPin：：連線**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)，並將指標傳遞至輸入圖釘。
2.  如果輸出 pin 接受連接，則會在輸入 pin 上呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 。
3.  如果輸入釘選也接受連接，連接嘗試就會成功，而且會連線到 pin。

當篩選準則為作用中時，某些 pin 可以中斷連接並重新連接。 這種類型的重新連接稱為 *動態* 重新連接。 如需詳細資訊，請參閱[動態 Graph 建立](dynamic-graph-building.md)。 不過，大部分的篩選器都不支援動態重新連接。

篩選通常會以下游順序連接，換句話說，篩選器的輸入接點會在其輸出圖釘之前連線。 篩選準則應該一律支援此連接順序。 某些篩選準則也會以相反的順序支援連接—輸出釘選，後面接著輸入圖釘。 例如，在連接 MUX 篩選器的輸入圖釘之前，可能可以將 MUX 篩選器的輸出圖釘連接至檔案寫入器篩選器。

當呼叫釘選 **連線** 或 **ReceiveConnection** 方法時，pin 必須確認它可以支援連接。 詳細資料取決於特定的篩選準則。 最常見的工作包括下列各項：

-   檢查媒體類型是否可接受
-   協調配置器
-   查詢其他 pin 以取得必要的介面。

 

 



