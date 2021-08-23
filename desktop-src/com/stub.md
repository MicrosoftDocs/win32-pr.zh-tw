---
title: 存根
description: 存根（如同 proxy）是由一或多個介面片段和管理員所組成。
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f182cd2d47eec18f129d53d57c283d54862660a126d2d9e171989695418b3a8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678421"
---
# <a name="stub"></a>存根

存根（如同 proxy）是由一或多個介面片段和管理員所組成。 每個介面存根都會提供程式碼，以 unmarshal 呼叫其中一個物件支援介面的參數和程式碼。 每個 stub 也提供內部通訊的介面。 存根管理員會持續追蹤可用的介面存根。

不過，存根和 proxy 之間有下列差異：

-   最重要的差異在於存根代表物件位址空間中的用戶端。
-   存根不會實作為匯總物件，因為不需要將用戶端視為單一單位;存根中的每個部分都是個別的元件。
-   介面存根是私用的，而非公用。
-   介面存根會執行 [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer)，而不是 [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer)。
-   存根不會封裝要封送處理的參數，而是在封送處理之後 unpackages 它們，然後封裝回復。

## <a name="structure-of-the-stub"></a>存根的結構

下圖顯示存根的結構。 每個介面存根都會連接到物件上的介面。 通道會將傳入訊息分派至適當的介面存根。 所有元件都會透過 [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer)（可存取 RPC 執行時間程式庫的介面）與通道通訊。

![顯示存根結構的螢幕擷取畫面。](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

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

[Proxy](proxy.md)
</dt> </dl>

 

 