---
title: 標記提供者
description: 標記提供者
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673100"
---
# <a name="moniker-providers"></a><span data-ttu-id="584d6-103">標記提供者</span><span class="sxs-lookup"><span data-stu-id="584d6-103">Moniker Providers</span></span>

<span data-ttu-id="584d6-104">一般情況下，當元件允許存取其中一個物件時，它應該是「標記提供者」，同時仍可控制物件的儲存體。</span><span class="sxs-lookup"><span data-stu-id="584d6-104">In general, a component should be a moniker provider when it allows access to one of its objects, while still controlling the object's storage.</span></span> <span data-ttu-id="584d6-105">如果元件即將推出可識別其物件的名字標記，它必須能夠執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="584d6-105">If a component is going to hand out monikers that identify its objects, it must be capable of performing the following tasks:</span></span>

-   <span data-ttu-id="584d6-106">在 [要求] 上，建立可識別物件的標記。</span><span class="sxs-lookup"><span data-stu-id="584d6-106">On request, create a moniker that identifies an object.</span></span>
-   <span data-ttu-id="584d6-107">當用戶端呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 時，啟用要系結的標記。</span><span class="sxs-lookup"><span data-stu-id="584d6-107">Enable the moniker to be bound when a client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on it.</span></span>

<span data-ttu-id="584d6-108">「標記提供者」必須建立適當的「 *標記」類別* 的標記來識別物件。</span><span class="sxs-lookup"><span data-stu-id="584d6-108">A moniker provider must create a moniker of an appropriate *moniker class* to identify an object.</span></span> <span data-ttu-id="584d6-109">「標記」類別會參考 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的特定執行，以定義所建立的標記類型。</span><span class="sxs-lookup"><span data-stu-id="584d6-109">The moniker class refers to a specific implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface that defines the type of moniker created.</span></span> <span data-ttu-id="584d6-110">雖然您可以執行 **IMoniker** 來建立新的「標記」類別，但通常不需要這樣做，因為 OLE 提供數個不同的「標記」類別，每個類別都有自己的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="584d6-110">While you can implement **IMoniker** to create a new moniker class, it is frequently unnecessary because OLE provides implementations of several different moniker classes, each with its own CLSID.</span></span> <span data-ttu-id="584d6-111">如需 OLE 提供之標記類別的描述，請參閱 [Ole 標記](ole-moniker-implementations.md) 。</span><span class="sxs-lookup"><span data-stu-id="584d6-111">See [OLE Moniker Implementations](ole-moniker-implementations.md) for descriptions of moniker classes that OLE provides.</span></span>

## <a name="related-topics"></a><span data-ttu-id="584d6-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="584d6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="584d6-113">標記用戶端</span><span class="sxs-lookup"><span data-stu-id="584d6-113">Moniker Clients</span></span>](moniker-clients.md)
</dt> <dt>

[<span data-ttu-id="584d6-114">OLE 標記執行</span><span class="sxs-lookup"><span data-stu-id="584d6-114">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




