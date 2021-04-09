---
title: 可連線物件介面
description: 可連線物件介面
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840792"
---
# <a name="connectable-object-interfaces"></a>可連線物件介面

可連線物件的支援需要四個介面：

-   可連線物件上的 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)
-   連接點物件上的 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint)
-   列舉值物件上的 [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints)
-   列舉值物件上的 [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections)

後兩個會定義為 **IConnectionPoint \*** 和 [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata)類型的標準枚舉器。

此外，可連線物件也可以選擇性地支援 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 和 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) ，以提供足夠的資訊給用戶端，讓用戶端可以在執行時間提供輸出介面的支援。

最後，用戶端必須提供可執行輸出介面的接收物件，這是可連線物件所定義的自訂 COM 介面。

如需詳細資訊，請參閱下列主題：

-   [使用 IConnectionPointContainer](using-iconnectionpointcontainer.md)
-   [使用 IConnectionPoint](using-iconnectionpoint.md)
-   [使用 IProvideClassInfo](using-iprovideclassinfo.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可連線物件的架構](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




