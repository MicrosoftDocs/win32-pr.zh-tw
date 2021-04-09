---
title: 使用 IConnectionPoint
description: 使用 IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7aa758ec1bd40233b1cc41a6c375ed296fc167
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024119"
---
# <a name="using-iconnectionpoint"></a>使用 IConnectionPoint

當用戶端有指向連接點的指標時，可以執行下列作業，以透過 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint)表示：

-   首先， [**IConnectionPoint：： GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) 會抓取連接點所支援的連出介面 IID。 當與 [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints)搭配使用時，此方法可讓用戶端檢查可連線物件上支援的所有傳出介面 iid。
-   其次，用戶端可以透過 [**IConnectionPoint：： GetConnectionPointContainer**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer)方法，從連接點流覽回到可連線物件的 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)介面。
-   第三，用戶端最感興趣的方法是 [**IConnectionPoint：： Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) 和 [**IConnectionPoint：： Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise)。 當用戶端想要將本身的接收物件連接至可連線物件時，用戶端會將接收器的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 指標 (或相同物件上的任何其他介面指標，) 為 **建議**。 連接點會查詢預期之特定輸出介面的接收。 如果接收上有該介面，則連接點會儲存介面指標。 從這個點一直到呼叫 **Unadvise** 為止，可連接的物件會在事件發生時，透過這個介面呼叫接收器。 若要中斷連接連接點的接收，用戶端會將從「 **建議** 」傳回的金鑰傳遞給 **Unadvise** 方法。 **Unadvise** 必須在接收器介面上呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。
-   最後，用戶端可以要求連接點透過 [**IConnectionPoint：： EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections)列舉存在的所有連接。 這個方法會使用不同的參考計數來建立列舉值物件 () 傳回 [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) 指標。 當不再需要列舉值時，用戶端必須呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。 此外，列舉值會傳回一系列的 [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata) 結構，每個連接各一。 每個結構會使用接收的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 指標以及原先從「 [**建議**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise)」傳回的連接金鑰來描述一個連接。 使用這些接收介面指標完成時，用戶端必須在 **CONNECTDATA** 結構中傳回的每個指標上呼叫 **Release** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可連線物件介面](connectable-object-interfaces.md)
</dt> </dl>

 

 