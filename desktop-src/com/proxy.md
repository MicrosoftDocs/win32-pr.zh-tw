---
title: Proxy
description: Proxy 位於呼叫進程的位址空間中，並作為遠端物件的代理。
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0478ce9ad1e08d343f1536fcd4bba63e59ae0fd229390be31c978bd20f737b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130002"
---
# <a name="proxy"></a>Proxy

Proxy 位於呼叫進程的位址空間中，並作為遠端物件的代理。 從呼叫物件的觀點來看，proxy 就是物件。 一般而言，proxy 的角色是封裝介面參數，以呼叫其物件介面中的方法。 Proxy 會將參數封裝至訊息緩衝區，並將緩衝區傳遞至通道，以處理處理常式之間的傳輸。 Proxy 會實作為匯總或複合的物件。 它包含系統提供的管理員元件，稱為 proxy 管理員以及一或多個介面特定的元件，稱為 interface proxy。 介面 proxy 的數目等於已公開給該特定用戶端的物件介面數目。 用戶端若要遵守元件物件模型，proxy 就會顯示為真正的物件。

> [!Note]  
> 使用自訂封送處理時，您可以類似的方式執行 proxy，也可以直接與物件進行通訊，而不需要使用存根。

 

每個介面 proxy 都是元件物件，可針對其中一個物件的介面來執行封送處理常式代碼。 Proxy 代表提供封送處理常式代碼的物件。 每個 proxy 也會實 [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) 介面。 雖然 proxy 表示的物件介面是公用的，但 **IRpcProxyBuffer** 實作為私用，並且在 proxy 內部使用。 Proxy 管理員會持續追蹤介面 proxy，也會包含針對匯總控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面的公用執行。 每個介面 proxy 都可以存在於不同的 DLL 中，當它所支援的介面具體化至用戶端時，就會載入該 DLL。

## <a name="structure-of-the-proxy"></a>Proxy 的結構

下圖顯示的 proxy 結構支援屬於兩個介面的標準封送處理參數： IA1 和 IA2。 每個介面 proxy 都會針對匯總片段之間的內部通訊來執行 [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) 。 當 proxy 準備將其封送處理的參數傳遞至整個進程界限時，它會呼叫 [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) 介面中的方法，該介面是由通道所執行。 通道接著會將呼叫轉送至 RPC 執行時間程式庫，讓它可以在物件中到達其目的地。

![顯示 proxy 結構的圖表。](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[通道](channel.md)
</dt> <dt>

[物件間通訊](inter-object-communication.md)
</dt> <dt>

[封送處理詳細資料](marshaling-details.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[存根](stub.md)
</dt> </dl>

 

 