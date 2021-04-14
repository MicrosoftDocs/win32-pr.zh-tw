---
title: 執行 IClassFactory
description: 執行 IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382918"
---
# <a name="implementing-iclassfactory"></a><span data-ttu-id="af14f-103">執行 IClassFactory</span><span class="sxs-lookup"><span data-stu-id="af14f-103">Implementing IClassFactory</span></span>

<span data-ttu-id="af14f-104">當用戶端使用 CLSID 要求物件實例的建立時，第一個步驟是建立類別物件，這個中繼物件包含 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面的方法的執行。</span><span class="sxs-lookup"><span data-stu-id="af14f-104">When a client uses a CLSID to request the creation of an object instance, the first step is creation of a class object, an intermediate object that contains an implementation of the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface.</span></span> <span data-ttu-id="af14f-105">雖然 COM 提供數個實例建立函式，但這些函式的執行中的第一個步驟是建立類別物件。</span><span class="sxs-lookup"><span data-stu-id="af14f-105">While COM provides several instance creation functions, the first step in the implementation of these functions is the creation of a class object.</span></span>

<span data-ttu-id="af14f-106">因此，所有伺服器都必須執行 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面的方法，其中包含兩種方法：</span><span class="sxs-lookup"><span data-stu-id="af14f-106">As a result, all servers must implement the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface, which contains two methods:</span></span>

-   <span data-ttu-id="af14f-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance)。</span><span class="sxs-lookup"><span data-stu-id="af14f-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span></span> <span data-ttu-id="af14f-108">這個方法必須建立物件的未初始化實例，並將指標傳回物件上要求的介面。</span><span class="sxs-lookup"><span data-stu-id="af14f-108">This method must create an uninitialized instance of the object and return a pointer to a requested interface on the object.</span></span>
-   <span data-ttu-id="af14f-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver)。</span><span class="sxs-lookup"><span data-stu-id="af14f-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span></span> <span data-ttu-id="af14f-110">這個方法只會遞增類別物件上的參考計數，以確保伺服器留在記憶體中，而且在用戶端準備好執行這項作業之前，不會關閉它。</span><span class="sxs-lookup"><span data-stu-id="af14f-110">This method just increments the reference count on the class object to ensure that the server stays in memory and does not shut down before the client is ready for it to do so.</span></span>

<span data-ttu-id="af14f-111">為了讓伺服器負責自己的授權，COM 會定義 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)，以從 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)繼承其定義。</span><span class="sxs-lookup"><span data-stu-id="af14f-111">To enable a server to be responsible for its own licensing, COM defines [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), which inherits its definition from [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="af14f-112">因此，執行 **IClassFactory2** 的伺服器必須依照定義執行 **IClassFactory** 的方法。</span><span class="sxs-lookup"><span data-stu-id="af14f-112">Thus, a server implementing **IClassFactory2** must, by definition, implement the methods of **IClassFactory**.</span></span>

<span data-ttu-id="af14f-113">COM 也提供 helper 函式來執行跨進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="af14f-113">COM also provides helper functions for implementing out-of-process servers.</span></span> <span data-ttu-id="af14f-114">如需詳細資訊，請參閱 [跨進程伺服器執行](out-of-process-server-implementation-helpers.md)協助程式。</span><span class="sxs-lookup"><span data-stu-id="af14f-114">For more information, see [Out-of-Process Server Implementation Helpers](out-of-process-server-implementation-helpers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af14f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="af14f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af14f-116">COM 伺服器責任</span><span class="sxs-lookup"><span data-stu-id="af14f-116">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> <dt>

[<span data-ttu-id="af14f-117">授權和 IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="af14f-117">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 