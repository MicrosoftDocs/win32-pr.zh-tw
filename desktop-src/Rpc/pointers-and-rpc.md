---
title: 指標和 RPC
description: 使用指標做為 C 函數參數非常有效率。
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840520"
---
# <a name="pointers-and-rpc"></a><span data-ttu-id="c35b3-103">指標和 RPC</span><span class="sxs-lookup"><span data-stu-id="c35b3-103">Pointers and RPC</span></span>

<span data-ttu-id="c35b3-104">使用指標做為 C 函數參數非常有效率。</span><span class="sxs-lookup"><span data-stu-id="c35b3-104">It is very efficient to use pointers as C-function parameters.</span></span> <span data-ttu-id="c35b3-105">指標只會有幾個位元組，可用來存取大量的記憶體。</span><span class="sxs-lookup"><span data-stu-id="c35b3-105">The pointer costs only a few bytes and can be used to access a large amount of memory.</span></span> <span data-ttu-id="c35b3-106">不過，在分散式應用程式中，用戶端和伺服器程式位於不同的位址空間中，它們可以在不同的電腦上。</span><span class="sxs-lookup"><span data-stu-id="c35b3-106">However, in a distributed application, the client and server procedures reside in different address spaces—they can be on different computers.</span></span> <span data-ttu-id="c35b3-107">因此，用戶端和伺服器通常無法存取相同的記憶體空間。</span><span class="sxs-lookup"><span data-stu-id="c35b3-107">Therefore, the client and the server usually do not have access to the same memory space.</span></span>

<span data-ttu-id="c35b3-108">當其中一個遠端程式的參數是物件的指標時，用戶端必須將該物件的複本及其指標傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="c35b3-108">When one of the remote procedure's parameters is a pointer to an object, the client must transmit a copy of that object and its pointer to the server.</span></span> <span data-ttu-id="c35b3-109">如果遠端程式透過其指標修改物件，伺服器會傳回指標及其修改過的複本。</span><span class="sxs-lookup"><span data-stu-id="c35b3-109">If the remote procedure modifies the object through its pointer, the server returns the pointer and its modified copy.</span></span>

<span data-ttu-id="c35b3-110">MIDL 提供指標屬性，將所需的額外負荷和應用程式大小降到最低。</span><span class="sxs-lookup"><span data-stu-id="c35b3-110">MIDL offers pointer attributes to minimize the amount of required overhead and the size of your application.</span></span> <span data-ttu-id="c35b3-111">本節討論 MIDL 指標屬性的用途和用法。</span><span class="sxs-lookup"><span data-stu-id="c35b3-111">This section discusses the purpose and uses of MIDL pointer attributes.</span></span> <span data-ttu-id="c35b3-112">它也會提供 RPC 應用程式中指標處理的資訊。</span><span class="sxs-lookup"><span data-stu-id="c35b3-112">It also presents information on pointer handling in RPC applications.</span></span> <span data-ttu-id="c35b3-113">它分成下列主題：</span><span class="sxs-lookup"><span data-stu-id="c35b3-113">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="c35b3-114">指標種類</span><span class="sxs-lookup"><span data-stu-id="c35b3-114">Kinds of Pointers</span></span>](kinds-of-pointers.md)
-   [<span data-ttu-id="c35b3-115">指標和記憶體配置</span><span class="sxs-lookup"><span data-stu-id="c35b3-115">Pointers and Memory Allocation</span></span>](pointers-and-memory-allocation.md)
-   [<span data-ttu-id="c35b3-116">預設指標類型</span><span class="sxs-lookup"><span data-stu-id="c35b3-116">Default Pointer Types</span></span>](default-pointer-types.md)
-   [<span data-ttu-id="c35b3-117">指標屬性類型繼承</span><span class="sxs-lookup"><span data-stu-id="c35b3-117">Pointer-Attribute Type Inheritance</span></span>](pointer-attribute-type-inheritance.md)

 

 




