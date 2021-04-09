---
title: 正在進入執行狀態
description: 正在進入執行狀態
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932153"
---
# <a name="entering-the-running-state"></a><span data-ttu-id="e0441-103">正在進入執行狀態</span><span class="sxs-lookup"><span data-stu-id="e0441-103">Entering the Running State</span></span>

<span data-ttu-id="e0441-104">當内嵌物件轉換成執行中狀態時，物件處理常式必須找出並執行伺服器應用程式，才能利用只有伺服器提供的服務。</span><span class="sxs-lookup"><span data-stu-id="e0441-104">When an embedded object makes the transition to the running state, the object handler must locate and run the server application in order to utilize the services that only the server provides.</span></span> <span data-ttu-id="e0441-105">內嵌的物件會透過容器的要求（例如，需要繪製目前未快取的格式），或由 OLE 隱含地以回應叫用某些作業（例如當容器的使用者按兩下該物件時）隱含地置於執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="e0441-105">Embedded objects are placed in the running state either explicitly through a request by the container, such as a need to draw a format not currently cached, or implicitly by OLE in response to invoking some operation, such as when a user of the container double-clicks the object.</span></span>

<span data-ttu-id="e0441-106">當連結化物件轉換成執行中狀態時，此程式 *就稱為系結。*</span><span class="sxs-lookup"><span data-stu-id="e0441-106">When a linked object makes the transition into the running state, the process is known as *binding*.</span></span> <span data-ttu-id="e0441-107">在系結的過程中，物件處理常式會要求其儲存的「標記」找出連結的資料，然後執行伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="e0441-107">In the process of binding, the object handler asks its stored moniker to locate the link's data, then runs the server application.</span></span>

<span data-ttu-id="e0441-108">乍看之下，連結化物件的系結似乎不會比執行内嵌物件複雜。</span><span class="sxs-lookup"><span data-stu-id="e0441-108">At first glance, binding a linked object appears to be no more complicated than running an embedded object.</span></span> <span data-ttu-id="e0441-109">但是，下列點會使程式變得複雜：</span><span class="sxs-lookup"><span data-stu-id="e0441-109">However, the following points complicate the process:</span></span>

-   <span data-ttu-id="e0441-110">連結可以參考內嵌于另一個容器中的物件（或其部分）。</span><span class="sxs-lookup"><span data-stu-id="e0441-110">A link can refer to an object, or a portion thereof, that is embedded in another container.</span></span> <span data-ttu-id="e0441-111">這項功能暗示了可能的嵌套內嵌。</span><span class="sxs-lookup"><span data-stu-id="e0441-111">This capability implies a potential for nested embeddings.</span></span> <span data-ttu-id="e0441-112">解析這類階層的參考需要以遞迴方式從最右邊的成員開始，以遞迴方式進行 *複合的標記*。</span><span class="sxs-lookup"><span data-stu-id="e0441-112">Resolving references to such a hierarchy requires recursively traversing a *composite moniker*, beginning with the rightmost member.</span></span>
-   <span data-ttu-id="e0441-113">當連結來源正在執行時，OLE 會系結至物件的執行中實例，而不是執行另一個實例。</span><span class="sxs-lookup"><span data-stu-id="e0441-113">When the link source is running, OLE binds to the running instance of the object rather than running another instance.</span></span> <span data-ttu-id="e0441-114">如果是內嵌的内嵌物件，其中一個是連結來源，則 OLE 必須能夠在任何時間點系結至已在執行中的物件。</span><span class="sxs-lookup"><span data-stu-id="e0441-114">In the case of nested embedded objects, one of which is the link source, OLE must be able to bind to an already running object at any point.</span></span>
-   <span data-ttu-id="e0441-115">執行物件需要存取物件的儲存區域。</span><span class="sxs-lookup"><span data-stu-id="e0441-115">Running an object requires accessing the storage area for the object.</span></span> <span data-ttu-id="e0441-116">當内嵌物件執行時，OLE 會在載入程式期間接收指向儲存體的指標，並將其傳遞至 OLE 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="e0441-116">When an embedded object is run, OLE receives a pointer to the storage during the load process, which it passes on to the OLE server application.</span></span> <span data-ttu-id="e0441-117">不過，針對連結的物件，並沒有可存取儲存體的標準介面。</span><span class="sxs-lookup"><span data-stu-id="e0441-117">For linked objects, however, there is no standard interface for accessing storage.</span></span> <span data-ttu-id="e0441-118">OLE 伺服器應用程式可能會使用檔案系統介面或其他機制。</span><span class="sxs-lookup"><span data-stu-id="e0441-118">The OLE server application may use the file system interface or some other mechanism.</span></span>

 

 




