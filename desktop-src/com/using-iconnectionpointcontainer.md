---
title: 使用 IConnectionPointContainer
description: 使用 IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a8d53e9051796cafa4a8c7825d810b18784d58a4dd5d531eb38872b87cb32c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992028"
---
# <a name="using-iconnectionpointcontainer"></a>使用 IConnectionPointContainer

可連線物件會執行 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (並透過 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 公開它) 來指出輸出介面是否存在。 針對每個輸出介面，可連線物件會管理連接點子物件，其本身會執行 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint)。 因此，可連接的物件會包含連接點，因此會命名為 **IConnectionPointContainer** 和 **IConnectionPoint**。

透過 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)，用戶端可以執行兩個作業。 首先，如果用戶端已經有它所支援之輸出介面的 IID，則可以使用 [**IConnectionPointContainer：： FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint)找出 iid 的對應連接點。 用戶端無法直接查詢連接點，因為可連線物件與其包含的連接點之間的容器/自主關聯性。 基本上，當用戶端知道 IID 時， **FindConnectionPoint** 就是輸出介面的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 。

其次，用戶端可以透過 [**IConnectionPointContainer：： EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints)來列舉可連線物件內的所有連接點。 這個方法會傳回個別列舉值物件的 [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) 介面指標。 透過 [**IEnumConnectionPoints：： Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next)，用戶端可以取得每個連接點的 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) 介面指標。

用戶端取得 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) 介面之後，必須呼叫 [**IConnectionPoint：： GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) 來判斷每個連接點所支援之輸出介面的 IID。 如果用戶端已支援該連出介面，則可以建立連線。 否則，它仍可支援傳出介面，方法是使用可連線物件類型程式庫中的資訊，在執行時間提供支援。 這項技術需要可連線物件支援 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 介面。  (參閱 [使用 IProvideClassInfo](using-iprovideclassinfo.md)。 ) 

因為列舉值是個別的物件，所以當不再需要列舉值時，用戶端必須呼叫 **IEnumConnectionPoints：： Release** 。 此外，每個連接點都是一個物件，其中包含來自包含可連線物件的不同參考計數。 因此，用戶端也必須針對透過列舉值或透過 [**FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint)存取的每個連接點呼叫 IConnectionPoint：： Release。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可連線物件介面](connectable-object-interfaces.md)
</dt> </dl>

 

 




