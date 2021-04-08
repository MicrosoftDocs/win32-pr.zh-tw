---
title: 名字
description: COM 中的名字標記不只是識別物件 \ 郵件的方式; 也會將標記實作為物件。
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020881"
---
# <a name="monikers"></a><span data-ttu-id="13128-103">名字</span><span class="sxs-lookup"><span data-stu-id="13128-103">Monikers</span></span>

<span data-ttu-id="13128-104">COM 中的名字標記並不只是識別物件的方式，也就是將標記實作為物件。</span><span class="sxs-lookup"><span data-stu-id="13128-104">A moniker in COM is not only a way to identify an object—a moniker is also implemented as an object.</span></span> <span data-ttu-id="13128-105">這個物件提供的服務可讓元件取得以標記識別之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="13128-105">This object provides services allowing a component to obtain a pointer to the object identified by the moniker.</span></span> <span data-ttu-id="13128-106">此 *進程稱為系結。*</span><span class="sxs-lookup"><span data-stu-id="13128-106">This process is referred to as *binding*.</span></span>

<span data-ttu-id="13128-107">「名字」是實 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的物件，而且通常會在 dll 中實作為元件物件。</span><span class="sxs-lookup"><span data-stu-id="13128-107">Monikers are objects that implement the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface and are generally implemented in DLLs as component objects.</span></span> <span data-ttu-id="13128-108">有兩種方式可以查看標記的使用方式：做為標記用戶端，這是使用標記來取得其他物件指標的元件;和作為「標記提供者」（provider），此元件會提供將其物件識別為「標記用戶端」的名字</span><span class="sxs-lookup"><span data-stu-id="13128-108">There are two ways of viewing the use of monikers: as a moniker client, a component that uses a moniker to get a pointer to another object; and as a moniker provider, a component that supplies monikers identifying its objects to moniker clients.</span></span>

<span data-ttu-id="13128-109">無論物件是在同一部電腦或整個網路中，OLE 都會使用它來連接和啟始物件。</span><span class="sxs-lookup"><span data-stu-id="13128-109">OLE uses monikers to connect to and activate objects, whether they are in the same machine or across a network.</span></span> <span data-ttu-id="13128-110">很重要的用途是針對網路連接。</span><span class="sxs-lookup"><span data-stu-id="13128-110">A very important use is for network connections.</span></span> <span data-ttu-id="13128-111">它們也可用來識別、連接和執行 OLE 複合檔案連結化物件。</span><span class="sxs-lookup"><span data-stu-id="13128-111">They are also used to identify, connect to, and run OLE compound document link objects.</span></span> <span data-ttu-id="13128-112">在此情況下，連結來源會作為「標記提供者」，而保留連結化物件的容器則會作為「標記用戶端」。</span><span class="sxs-lookup"><span data-stu-id="13128-112">In this case, the link source acts as the moniker provider and the container holding the link object acts as the moniker client.</span></span>

<span data-ttu-id="13128-113">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="13128-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="13128-114">標記用戶端</span><span class="sxs-lookup"><span data-stu-id="13128-114">Moniker Clients</span></span>](moniker-clients.md)
-   [<span data-ttu-id="13128-115">標記提供者</span><span class="sxs-lookup"><span data-stu-id="13128-115">Moniker Providers</span></span>](moniker-providers.md)
-   [<span data-ttu-id="13128-116">OLE 標記執行</span><span class="sxs-lookup"><span data-stu-id="13128-116">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)

## <a name="related-topics"></a><span data-ttu-id="13128-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="13128-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13128-118">元件物件模型</span><span class="sxs-lookup"><span data-stu-id="13128-118">The Component Object Model</span></span>](the-component-object-model.md)
</dt> </dl>

 

 




