---
description: Select 函數用來判斷集合中一或多個通訊端的狀態。 針對每個通訊端，呼叫端可以要求讀取、寫入或錯誤狀態的相關資訊。 一組通訊端是由 FD \_ 集結構所表示。
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Select 上有多個提供者限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2556d98aea60e6fa822f9e3df57cc142c33491d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113040"
---
# <a name="multiple-provider-restrictions-on-select"></a><span data-ttu-id="108ab-105">Select 上有多個提供者限制</span><span class="sxs-lookup"><span data-stu-id="108ab-105">Multiple Provider Restrictions on Select</span></span>

<span data-ttu-id="108ab-106">[**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select)函數用來判斷集合中一或多個通訊端的狀態。</span><span class="sxs-lookup"><span data-stu-id="108ab-106">The [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function is used to determine the status of one or more sockets in a set.</span></span> <span data-ttu-id="108ab-107">針對每個通訊端，呼叫端可以要求讀取、寫入或錯誤狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="108ab-107">For each socket, the caller can request information on read, write, or error status.</span></span> <span data-ttu-id="108ab-108">一組通訊端是由 [**FD \_ 集**](/windows/desktop/api/winsock/nf-winsock-fd_set) 結構所表示。</span><span class="sxs-lookup"><span data-stu-id="108ab-108">A set of sockets is indicated by an [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structure.</span></span>

<span data-ttu-id="108ab-109">Windows 通訊端2可讓應用程式使用多個服務提供者，但 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 函式僅限於一組與單一服務提供者相關聯的通訊端。</span><span class="sxs-lookup"><span data-stu-id="108ab-109">Windows Sockets 2 allows an application to use more than one service provider, but the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function is limited to a set of sockets associated with a single service provider.</span></span> <span data-ttu-id="108ab-110">這不會以任何方式限制應用程式必須透過多個提供者來開啟多個通訊端。</span><span class="sxs-lookup"><span data-stu-id="108ab-110">This does not in any way restrict an application from having multiple sockets open through multiple providers.</span></span>

<span data-ttu-id="108ab-111">有兩種方式可判斷跨多個服務提供者的一組通訊端狀態：</span><span class="sxs-lookup"><span data-stu-id="108ab-111">There are two ways to determine the status of a set of sockets that spans more than one service provider:</span></span>

-   <span data-ttu-id="108ab-112">使用 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) 或 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式時，會採用封鎖語義。</span><span class="sxs-lookup"><span data-stu-id="108ab-112">Using the [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) or [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) functions when blocking semantics are employed.</span></span>
-   <span data-ttu-id="108ab-113">當採用非封鎖作業，而且應用程式已經在使用 Windows 訊息抽取時，使用 [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) 函式。</span><span class="sxs-lookup"><span data-stu-id="108ab-113">Using the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function when nonblocking operations are employed and the application is already using a Windows message pump.</span></span>

<span data-ttu-id="108ab-114">當應用程式需要在橫跨多個提供者的一組通訊端上使用封鎖語義時，建議使用 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) 。</span><span class="sxs-lookup"><span data-stu-id="108ab-114">When an application needs to use blocking semantics on a set of sockets that spans multiple providers, [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) is recommended.</span></span> <span data-ttu-id="108ab-115">應用程式也可以使用 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式，此函式可讓 FD \_ XXX 網路事件 (參閱 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) ，以便與事件物件建立關聯，並從事件物件架構內處理 (如重迭的 [i/o 和事件物件](overlapped-i-o-and-event-objects-2.md)) 所述。</span><span class="sxs-lookup"><span data-stu-id="108ab-115">The application can also use the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function, which allows the FD\_XXX network events (see [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) to associate with an event object and be handled from within the event object paradigm (described in [Overlapped I/O and Event Objects](overlapped-i-o-and-event-objects-2.md)).</span></span>

<span data-ttu-id="108ab-116">[**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect)函式不會限制為單一提供者，因為它採用單一通訊端描述元作為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="108ab-116">The [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function is not restricted to a single provider because it takes a single socket descriptor as an input parameter.</span></span> <span data-ttu-id="108ab-117">不過請注意， [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式在 **WSAAsyncSelect** 方面提供更佳的效能和擴充性，因為使用 Winsock 事件訊息來維護訊息提取的額外負荷，會隨著使用的通訊端總數增加而增加。</span><span class="sxs-lookup"><span data-stu-id="108ab-117">Note however, that [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function offers better performance and scalability over **WSAAsyncSelect** as the overhead of maintaining the message pump with Winsock event messages increases as the total number of sockets being used increases.</span></span>

 

 



