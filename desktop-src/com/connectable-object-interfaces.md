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
# <a name="connectable-object-interfaces"></a><span data-ttu-id="d37e1-103">可連線物件介面</span><span class="sxs-lookup"><span data-stu-id="d37e1-103">Connectable Object Interfaces</span></span>

<span data-ttu-id="d37e1-104">可連線物件的支援需要四個介面：</span><span class="sxs-lookup"><span data-stu-id="d37e1-104">Support for connectable objects requires support for four interfaces:</span></span>

-   <span data-ttu-id="d37e1-105">可連線物件上的 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)</span><span class="sxs-lookup"><span data-stu-id="d37e1-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) on the connectable object</span></span>
-   <span data-ttu-id="d37e1-106">連接點物件上的 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint)</span><span class="sxs-lookup"><span data-stu-id="d37e1-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) on the connection point object</span></span>
-   <span data-ttu-id="d37e1-107">列舉值物件上的 [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints)</span><span class="sxs-lookup"><span data-stu-id="d37e1-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) on an enumerator object</span></span>
-   <span data-ttu-id="d37e1-108">列舉值物件上的 [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections)</span><span class="sxs-lookup"><span data-stu-id="d37e1-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) on an enumerator object</span></span>

<span data-ttu-id="d37e1-109">後兩個會定義為 **IConnectionPoint \*** 和 [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata)類型的標準枚舉器。</span><span class="sxs-lookup"><span data-stu-id="d37e1-109">The latter two are defined as standard enumerators for the types **IConnectionPoint \*** and [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span></span>

<span data-ttu-id="d37e1-110">此外，可連線物件也可以選擇性地支援 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 和 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) ，以提供足夠的資訊給用戶端，讓用戶端可以在執行時間提供輸出介面的支援。</span><span class="sxs-lookup"><span data-stu-id="d37e1-110">Additionally, the connectable object can optionally support [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) to provide enough information to a client so that the client can provide support for the outgoing interface at run time.</span></span>

<span data-ttu-id="d37e1-111">最後，用戶端必須提供可執行輸出介面的接收物件，這是可連線物件所定義的自訂 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="d37e1-111">Finally, the client must provide a sink object that implements the outgoing interface, which is a custom COM interface defined by the connectable object.</span></span>

<span data-ttu-id="d37e1-112">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="d37e1-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d37e1-113">使用 IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="d37e1-113">Using IConnectionPointContainer</span></span>](using-iconnectionpointcontainer.md)
-   [<span data-ttu-id="d37e1-114">使用 IConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="d37e1-114">Using IConnectionPoint</span></span>](using-iconnectionpoint.md)
-   [<span data-ttu-id="d37e1-115">使用 IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="d37e1-115">Using IProvideClassInfo</span></span>](using-iprovideclassinfo.md)

## <a name="related-topics"></a><span data-ttu-id="d37e1-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="d37e1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d37e1-117">可連線物件的架構</span><span class="sxs-lookup"><span data-stu-id="d37e1-117">Architecture of Connectable Objects</span></span>](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




