---
title: 開發 RPC-Message 佇列應用程式
description: 若要在 RPC 應用程式中利用 MSMQ 傳輸，很少需要投入很多時間。
ms.assetid: 1ea97df8-cdf5-43b8-88aa-9e8fa6ae845a
keywords:
- 遠端程序呼叫 RPC、工作、開發訊息佇列應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09cf7b3a5d6d33facebb1de6a3c0f37eb9ba48f2afa54e6143ad5cb0169ad601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930571"
---
# <a name="developing-rpc-message-queuing-applications"></a>開發 RPC-Message 佇列應用程式

若要在 RPC 應用程式中利用 MSMQ 傳輸，很少需要投入很多時間。 針對同步訊息，您只需要將訊息佇列傳輸 ([**ncadg \_ mq**](/windows/desktop/Midl/ncadg-mq)) 指定為通訊協定順序。 **Ncadg \_ mq** 通訊協定支援所有標準資料包功能，但廣播呼叫除外。 此外，請注意，目前訊息佇列傳輸不支援動態端點。

藉由將 \[ [**訊息**](/windows/desktop/Midl/message) \] 屬性套用至 IDL 檔案中的遠端過程聲明，您會自動針對這些呼叫來執行非同步模式訊息佇列。 這可讓用戶端和伺服器應用程式控制許多與訊息和訊息佇列相關聯的屬性，包括：

-   服務品質
-   收條的確認
-   日誌記錄
-   呼叫優先順序
-   伺服器進程佇列的持續性

服務品質是為了將呼叫傳遞給伺服器進程所做的努力。 快速傳遞將會排入記憶體中，因此相當快速，但如果電腦或網路連線在錯誤的時間中斷，呼叫就會遺失。 可復原的傳遞將會張貼到磁片檔案，直到傳遞為止，因此即使在電腦損毀的情況下，呼叫也不會遺失。 這會提供保證的傳遞，但在每次呼叫寫入磁片時，效能會降低。

您也可以在傳回之前，告知 MSMQ 傳輸等候呼叫已到達目的地 (server) 佇列。 選擇這個選項會封鎖用戶端，直到伺服器確認呼叫為止，否則控制權會在進行呼叫時立即回到用戶端。

藉由使用日誌，可將通話記錄至磁片。 如果開啟日誌功能，每個呼叫都會記錄到磁片上，因為它會傳送至伺服器進程的下一個躍點。

呼叫優先順序可以與 RPC \[ [**message**](/windows/desktop/Midl/message) \] function 屬性搭配使用，以允許優先順序較高的呼叫優先于較低優先順序的呼叫，即使高優先順序呼叫稍後抵達也是如此。 呼叫優先順序也可使用同步 RPC 以有限的方式運作，但同步 RPC 呼叫無法以與非同步呼叫相同的方式堆疊。

用戶端進程會藉由呼叫 [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)來控制上述所有屬性。 一旦設定之後，這些屬性就會維持有效，直到在另一次呼叫 **RpcBindingSetOption** 時才會變更。

RPC 伺服器進程可以控制其接收佇列的存留期。 根據預設，佇列會在伺服器進程結束時刪除。 不過，在設定端點時，伺服器進程可以使用 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) ，告知傳輸允許佇列繼續存在，以及即使在伺服器進程未執行時也接受呼叫要求。 在此情況下，呼叫會排入佇列，並于稍後在伺服器進程恢復上線時執行。

> [!Note]  
> 如果您 \[ [](/windows/desktop/Midl/message) \] 在介面中使用非同步訊息呼叫，則必須先呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)或 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)來註冊介面，然後再呼叫 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) **(ncadg \_ mq)**。 一旦開啟通訊協定順序，任何已在佇列中等候伺服器的呼叫，就會開始讀取佇列。 如果對應的 RPC 介面尚未註冊，則呼叫會失敗。 如果您已設定遠端程序呼叫的永久端點、伺服器已經關閉，而且用戶端繼續傳送呼叫給伺服器，就會發生這種情況。 這些呼叫會堆疊在佇列中，等候在伺服器重新上線時讀取。

 

如需詳細資訊，請參閱 [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)、 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)和 \[ [**message**](/windows/desktop/Midl/message) \] [**ncadg \_ mq**](/windows/desktop/Midl/ncadg-mq)。

 

 